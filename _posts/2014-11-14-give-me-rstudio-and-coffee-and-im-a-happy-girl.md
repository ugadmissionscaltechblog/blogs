---
layout: post
author: Emily
image: /old_images/caltech_as_it_happens/6a0105349b8251970b01b7c702e04c970b.png
title: Give me RStudio and coffee and I'm a happy girl. 
categories: [research]
status: Publish
date: 2014-11-14
---


I get distracted pretty easily. I read an op-ed letter in the [New York Times](https://www.nytimes.com/2014/11/02/opinion/sunday/a-natural-fix-for-adhd.html?src=me&amp;module=Ribbon&amp;version=context&amp;region=Header&amp;action=click&amp;contentCollection=Most%20Emailed&amp;pgtype=article) last week that described attention disorders as manifestations of evolutionary tendencies to seek out stimulating activities. The author insists that people who have short attention spans just need to find activities that they, personally, find interesting, and they can focus as sharply as anyone.

That's why, instead of doing problem sets, I've been building data-analysis webapps for the past 6 hours.

Screenshot of an app I made with Shiny, an R package for building data webapps. stockVis is an app you can build using the Shiny [tutorial](https://shiny.rstudio.com/tutorial/).

I LOVE playing with code. I realized this past summer that wet-lab microbiology research moves much too slowly for my liking, and switched my major from bioengineering to computer science. Now I can work on projects that I can test immediately, instead of doing one experiment a day (or a week) and spending most of my time waiting for proteins and RNA to incubate.

More than I love playing with code, I LOVE playing with data. The data scientist in me loves finding patterns in chaos of cluttered .csv files of raw data and turning them into beautiful images that communicate findings at a single glance. The research scientist in me looks at the patterns I find and goes "hmm correlation...further study needed to determine causation."

Anyway, I saw a headline a few weeks ago on the Wall Street Journal's website, that was something like, "Stocks Plunge Over Ebola Fears." I wanted to see how true this is, over time. New Ebola cases are still being recorded, afterall, and we don't seem to be in the midst of a financial crisis.

I scraped some Ebola case reporting data from Wikipedia (taken originally from the WHO), and used the "quantmod" and "shiny" R packages to create a Shiny webapp that compares stock prices for various stock and index symbols to the number of reported Ebola cases in West Africa on the same dates. I'm having some trouble plotting both lines on the same plot, so this is a rudimentary comparison. It'll look much better when I can figure out how to cleanly plot both data sets on the same plot, with two different Y axes. Also, I've got a weird bug where my Ebola cases plot is plotting the first data point at the end of the X axis, but the rest of the points in the correct order (I am using the "ggplot2" package). Anybody know how I did that? Brownie points if you comment with a solution!

![](/old_images/caltech_as_it_happens/6a0105349b8251970b01b7c702eb5b970b.png)
You can check out my webapp here:[https://techgrrrl.shinyapps.io/EbolavsStocks/](https://techgrrrl.shinyapps.io/EbolavsStocks/)

Some cool patterns: The DOW index took a tumble around October 13th, and hasn't fully recovered, which is suspiciously also when the NBI (NASDAQ Biotechnologies Index) started to soar. This is about the time period when the total recorded cases of Ebola in West Africa hit 10,000.

Sadly, a lot of Yahoo Finance data isn't available through .csv right now, not sure why. So not all ticker symbols are working with my webapp. Play around with it, though, and let me know if you find anything cool looking.

All of my code is available on [GitHub](https://github.com/EmilyMazo/Ebola-vs.-Stocks/tree/master). Feel free to fork and play around with it, and let me know if you have any corrections for me!

