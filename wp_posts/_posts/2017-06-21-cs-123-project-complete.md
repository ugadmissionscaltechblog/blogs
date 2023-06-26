---
title: CS 123 Project Complete!
image: /wp-content/uploads/old_images/caltech_as_it_happens/6a0105349b8251970b01b8d28b2022970c.png
date: 2017-06-21
categories: 668
author: Emily
---


I finally finished writing up my CS 123 (projects in databases) project from this term. I've posted about it a few times, but I wanted to share with you the entire thing!

I’m a really big fan of databases. I think it’s because the work is low-level enough that I feel like I have control over all data storage, all logic, and all concurrency issues, but high-level enough that I don’t have to deal with registers. I also love that it’s work that is applicable to every possible other project. Want to build anything that isn’t a static webpage? Get you some database.

That’s actually what drove me towards this project to begin with. Last fall, I worked with two other Caltech students to build a live-updating data visualization dashboard for tweets about the election (RIP). I designed the architecture of the project and set everything up on AWS. We used a couple of EC2 instances to connect to the Twitter Public Streaming API, ran a couple of machine learning models that we’d trained on the tweets that came through, aggregated the models’ scores, and updated a DynamoDB instance with the aggregates. We used Elastic Beanstalk to host our Node app, which read data out of DynamoDB and used D3.js to update our dashboard. We had a couple of visualizations, illustrating differences in tweet volume, sentiment, and vocabulary between twitter users with “liberal” and “conservative” ideologies (classified using our ML models) on four different topics concerning the election and election day. 


![](/old_images/caltech_as_it_happens/6a0105349b8251970b01b7c900fa5a970b.png)


![](/old_images/caltech_as_it_happens/6a0105349b8251970b01b8d28b202a970c.png)
*These are some screenshots of our visualizations of tweets from inside of the USA containing keywords about polling places at 8pm on 11/09/2017*. 

That project was really fun. I had the chance to learn some web development, a little bit of devops (bless Elastic Beanstalk for saving me from most of that, since I had four weeks to build this whole project and devops is way beyond my current skillset), and a little bit of data viz. One of my biggest takeaways from this project was how many options there were for setting up streaming data pipelines, and how complicated they were to set up. 

Note that our AWS architecture involved three different services, and I’d hacked it together in about two weeks. I was positive that there would have been an easier way to set up a data pipeline and not have to worry about learning how to use NoSQL databases, or having to use a million Amazon products. In my research for pipeline solutions, I ran across a couple of options, like Spark Streaming and PipelineDB. I was inspired by these solutions (particularly PipelineDB), since its ability to stream data into relational databases made me significantly more comfortable. What I was really looking for was a filter between the firehose of a data stream and the calm, organized environment of a relational database. I know I can handle databases, and I know I can create apps that read data from databases, so I wanted a tool that would put me back in my comfort zone. 

So, I built one!

**“What do you mean, you built one?”**

I mean I was inspired by other streaming SQL solutions to build my own method of turning streaming data into organized records in a relational database. I built my streaming solution on top of NanoDB, a relational database built by [Donnie Pinkston](https://users.cms.caltech.edu/donnie/), a lecturer at Caltech. Donnie built NanoDB for instructional purposes, and during winter 2017 I took his Relational Database Implementation class, where he deleted large chunks of the relational database system and we had to reimplement them. We worked on join planning, plan optimization, table statistics and plan costing, and B+ tree indexes, among other things. After taking this class, I was very familiar with the NanoDB codebase (written in Java), and felt it would save time to write my streaming solution on top of this database system instead of, say, Postgres. 

I call my database TrickleDB (because it’s a Nano stream, heh). TrickleDB can be used to connect to any source of JSON data and stream data into a relational database. It can also be used to create tables of streaming aggregate functions, which can track the data stream over time. It is functional and I am proud of it and I wanted to share its architecture with the world because designing this software was the most fun I’ve ever had in front of a computer (and yes, I do watch Silicon Valley on HBONow). 

**Design Choices**

The TrickleDB system is modeled after a tree hierarchy. There is one global StreamManager object, instantiated on startup, which can have zero or more Stream objects. Each Stream object can have zero or more StreamView objects, and must have one Source object.


![](/old_images/caltech_as_it_happens/6a0105349b8251970b01b8d28b203c970c.png)
*A class diagram of the four objects that make up the TrickleDB system.*

To set up the system, a user must start a NanoDB server, which instantiates the StreamManager, and then use the following SQL: 

`CREATE STREAM *tweets* SOURCE *https://www.twitter.com/api/tech_grrrl* ( tweet_id INT, number_of_likes INT, text VARCHAR(140) );`

This command creates a new Stream object. The Stream creates a new Source object, which operates a connection to the URL passed in with the command. The Stream also creates a “buffer table,” a relational database table with a schema based off of the column names and data types passed in with the CREATE STREAM command (plus two extra attributes for the arrival timestamp, and a boolean that tracks if the record has been “processed”). These column names must be identical to the key names in the JSON data the URL will be POSTing. This is because the Source parses each new JSON event over its connection and generates SQL INSERT statements out of the key names and values in the JSON data. The target of the INSERT statements is the Stream’s buffer table. The Source stores these INSERT statements (as strings) in a circular FIFO queue (its “buffer”). 

On a trigger (using the Quartz Java package), the StreamManager will tell the Stream to clear its buffer. The Stream will then access its Source’s buffer and execute every INSERT statement inside, using the NanoDB server. This populates the Stream’s buffer table with records consisting of the raw data coming over the Source’s connection.

To create a StreamView, the user will use a command like this: 

`CREATE STREAMVIEW *tweets_aggregate* ON *tweets* ( SUM(number_of_likes) );`

This command creates a new StreamView object that belongs to the Stream *tweets*. This StreamView creates a “view table” with a schema based on the passed-in aggregate functions on attributes of the Stream’s schema (in this case, SUM(number_of_likes)). The StreamView registers all of the aggregate functions that it’s schema needs to keep track of, and passes this information to the Stream. For example, *tweets_aggregate* will pass “SUM(number_of_likes)” to the *tweets* Stream, but if *tweets_aggregate* were tracking an average instead of a sum, it would pass SUM and COUNT to its Stream. 


![](/old_images/caltech_as_it_happens/6a0105349b8251970b01b7c900fa6f970b.png)
*A sequence diagram illustrating the actions taken by the TrickleDB system, shown on the right, upon user input in the form of SQL commands, shown on the left.*

The Stream uses the names of the aggregate functions from all of its StreamViews to create a temporary table (whose schema contains all of these aggregate functions). Periodically, when triggered by the StreamManager, the Stream will perform these aggregate functions on its buffer table and insert all the aggregate values into the temp table. The Stream will then trigger the method “performComplexAggregates()” in each of its StreamViews. Each StreamView will search the Stream’s temporary table for the aggregates that it is tracking, and will coalesce the partial aggregate data with the aggregate data it has already collected over time. For example, if *tweets_aggregate* has tracked 123 likes on all of my tweets since its instantiation, and in the period of time between the last time the Stream performed aggregation on its buffer table and now, the buffer table contains the value “6” for the attribute “SUM(number_of_likes)”, then “performComplexAggregates()” would coalesce these two values and update *tweets_aggregate.SUM(number_of_likes)* to be equal to 129. After each StreamView has completed its updates, the Stream marks all of the data in its buffer table as “processed.”

The StreamManager handles garbage collection on a separate Quartz trigger, periodically deleting “processed” data from each Stream’s buffer table. 


![](/old_images/caltech_as_it_happens/6a0105349b8251970b01b7c900fa78970b.png)
*A sequence diagram indicating all actions taken by the TrickleDB system. The pink boxes indicate triggers and jobs implemented using the Quartz package, which run periodically without user input. Except for instantiation using CREATE commands, the entire TrickleDB system runs without user interference, ingesting data from the Source’s connection, aggregating the data in the Stream, and coalescing the partial aggregates with the running aggregates in the StreamView.*

Here is an example of how data flows through the TrickleDB system. On the left is a representation of the various objects inside of TrickleDB, including the StreamManager, two Streams, each Stream’s Source, and each Stream’s StreamViews. On the right is a representation of how data that begins in JSON format from the Source’s connection is transformed into a streaming aggregate in the StreamView’s view table. The colored boxes that overlap the left and right sides of the diagram delineate between the forms of data each object (on the left) stores or transforms. 


![](/old_images/caltech_as_it_happens/6a0105349b8251970b01b7c900fa7f970b.png)
*The colored boxes represent the form that data takes during each step of processing. The blue box represents the data received over the connection on the Source’s URL. The pink box represents the INSERT statement parsed from the raw JSON and stored in the Source’s circular FIFO queue (the buffer). The orange box represents 1. The record in the Stream’s buffer table, 2. The INSERT statement used to populate the Stream’s temp table. The green box represents 1. The record of aggregates in the Stream’s temp table, and 2. The coalesced record in the StreamView’s view table.*

I hope at least some of you found this interesting! If so, you'll probably like Donnie Pinkston's CS 121, 122, and 123 class sequence here at Caltech.

