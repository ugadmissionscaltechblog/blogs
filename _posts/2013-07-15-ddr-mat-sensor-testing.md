---
layout: post
author: Laura
image: https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b01901e358778970b.png
title: DDR Mat Sensor Testing 
categories: [global]
status: Publish
date: 2013-07-15
---

We're almost ready to start building part of the DDR mats! The only non-circuit board materials we still need to get are sheet metal, plastic panels for arrows, and some screws. Recently I decided to test the sensor idea to make sure it would work. Based on previous DDR mat designs and instructions on DDR forums (like [here](https://zenius-i-vanisher.com/v5.2/viewthread.php?threadid=3350&amp;page=1)), we're first going to try to make sensors using steel mending plates and screws.

On the bottom of the DDR mat, we'll have high density 1/2" foam weatherstripping with flat head screws placed in the middle. The screws are slightly below the top of the weatherstripping. The steel mending plate will rest on top of the weatherstripping, and when someone presses down, the plate will compress the foam weatherstripping and make contact with the screws. 

Sensor diagram. Sheet metal plate rests on top of foam weatherstripping

A wire will be soldered to each screw, and another wire will be soldered to the steel mending plate. Most circuit boards for game controllers work by registering a button press when a circuit is completed, and it seems that the resistance in the circuit needs to be somewhere below 50-100 Ohms to register a button press. Having multiple screws and wiring them in parallel should help with this problem, since the most resistance in the circuit will probably come from the contact between the mending plate and screw head. Even if the metal contacts get dirty (which they probably will over time), having multiple screws in parallel should help keep the resistance low enough to register an arrow press. Additionally, the screws and sheet metal mending 
plates should be pretty easy to replace. Each screw will have its own wire to make replacing it, if needed, even easier.


![](https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0191042bad80970c.jpg)

![](https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0191042badbe970c.jpg)
An arrow panel will have four of these mending plate sensors; one centered on each edge. The most important edge is the edge closest to the center of the DDR mat, since that edge will be stepped on most often. For those edges, we'll use 6" mending plates instead of the 4" mending plates for the rest of the sides. It most likely won't make a difference in sensitivity, but we're putting them there just in case it does. Hopefully we will be able to build and test a few arrows in the next week!
