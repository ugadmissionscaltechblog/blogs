---
layout: post
author: Giordon Stark
image: https://d24slhcvzhzz82.cloudfront.net/old_images/6a0105349b8251970b0147e1b0ffb9970b.png
title: Dinosaurs, Curiosity, and Mandelbrot 
categories: [research]
status: Publish
date: 2011-01-19
---


Mighty readers of this awesome blog post, it is the second week of school! In other words, we have about 8 more weeks before this term ends. If you've never been on a quarter system, you'll enjoy all the benefits and punishments that come along with it when you come to Caltech. Some of the true benefits include being able to learn from a variety of professors on diverse subjects in short time periods (akin to the idea behind TED talks) as well as only have 10 weeks for a class you decide wasn't as interesting as it sounded. The obvious disadvantage is that you only have 10 weeks for a class you absolutely love (but that doesn't stop you from taking it time and time again by auditing it) and 1.5 times as many Midterm and Final exams as most other colleges. But in the case of Caltech, I'm positive that the 'pros' far outweigh the 'cons'.

In this week's blog post, I'll be talking a lot about Venerable OPI, a little bit about my Physics computational lab, and a little bit about TEDxCaltech [sadly, I wasn't able to go as I had a lab that day... but I'll provide links and awesome insight about it].

In chronological order, I'll start with my lab. This week's lab was to generate the Mandelbrot set using the equation Z(n+1) = Z(n)^2 + Z(0) where the 'escape count' of a point Z(0) is the number of iterations before Z(n+1) had a magnitude larger than 2 [ |Z(n+1)|&gt;2]. Mathematically, it's a pretty sound concept, not too hard to program in C++. The next part was to generate a matrix of numbers for which I would compute the escape counts of - using this matrix, I could loop through and create a matrix of escape counts. From this matrix of escape counts, I would assign a color value depending on how large the escape count is. Then, I would use an opensource plotting program [g2; https://g2.sourceforge.net/g2_ref/index.html] to generate a plot from the matrix of colors. The final part of the script was to have a variable resolution so I could make the plot bigger or smaller. To this part, I tried to compute a 100,000 pixel by 100,000 pixel resolution image of the Mandelbrot set.

I was only able to drag it left or right, if I had clicked anywhere else in the image, I would have executed a series of event listeners programmed to change the center of the image to where you clicked it or to zoom in/out. Finally, to finish this lab up, we simply had to calculate the area of the Mandelbrot set using the Pixel Counting method. This accounts to basically determining the number of pixels that don't escape (the black area in the image) and comparing it to the number of pixels that escaped (the colorful area of the image). Using some small images (300px by 300px up to 1000px by 1000px), I determined the area to be 1.607 +- 0.1. The best estimation is around 1.5, so I wasn't too far off. [More details on the pixel counting method can be found here: https://mrob.com/pub/muency/pixelcounting.html]. If you're interested in how it works with C++, you can post a comment and ask whatever questions you want.

TEDxCaltech!

TEDxCaltech was an independently organized TED talk that took place at Caltech on January 14th, 2011. There's really not much I can say about it that would be better than reading it from the source... so go there: https://tedxcaltech.com/! Some of the speakers included Pamela                          Björkman (amazing work with HIV), Shuki                          Bruck (a ridiculously awesome professor that I had for Information Systems and Technology class), John                          Preskill (my Quantum Mechanics professor last year - he absolutely loves Qubits), and current Caltech students like Jordan                          Theriot (she's in the class of 2012, my year!).

Also, Richard Feynman is THE man. Go read his lectures or something, get inspired in the world of Physics, Quantum Computation, and intellectual curiosity. 'Nuff said.

The next/last big event of the week is Venerable OPI: Day 0. (the computer scientist within me likes to start all numbers at 0 for simplicity). OPI is a pretty big deal at any house in Caltech. OPI stands for 'Our Private Interhouse'. Every year, each  house  picks a date and hosts a party for the entire campus. And during the term, we build and put the party together for that date. When I mean build, that does include getting music, food, t-shirts, flyers, propaganda.. but we're also BUILDING. Physically building a dance floor, building a theme to the party, painting the walls, stairs, elevated platforms, all that stuff. It's a pretty monumental task. So the way it works - we have **Grand Dragons** for the party: the leaders. This year, Venerable's **grand dragons** are Shamili Allam, Franz Sauer, and Me! Under the grand dragons, we delegate tasks to 'focus groups' in Construction, Art, Lighting, Music, Finance, etcetera. The people who are in charge of each separate section are called **Iguanas** and their job is to obey our every command and encourage lazy people to come help us build the party. For the remainder of this term, most of my talking about OPI will be focused on the Construction side, as that is my main area of expertise.

This year's theme is Jurassic Park - we'll be taking ideas and situations from Jurassic Park 1,2, and 3. But first, have a look see at our plans...


![](https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0148c7ba5c7f970c.jpg)


![](https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0148c7ba5d15970c.jpg)
This is a 3D view from the North-West corner of the party. As you can see, there is a series of elevated platforms around the party with a ramp connecting the bottom dance floor to the top. The gate is prominent in the top-right, a jeep on the right (the big light-green building is the wood shed, we keep all of our wood in there). On top of this wood shed, Andrew Gong (a Rudd) mounted a camera to take pictures constantly to create a timelapse video - more on this later. Finally you can see the electric fence that we plan to build (don't worry, it's a fake one! Caltech would never let us build a real one....)

We have some surprises planned in store that you can't see from these images. For example, we're planning on getting plexiglass so we can create a waterfall from the roof over the elevated platform so you can walk under a waterfall at the party! We're also building a couple of dinosaurs, including a T-Rex which will have broken through the fake electric fence and perhaps a fake bathroom stall (like in Jurassic Park 1). Most of these details are still in the mix and will be further solidifed and agreed upon as we get closer to the date of the party.

So "what's a timelapse?" you might ask. Well, I'm glad you asked! It's a series of pictures taken at fixed intervals for the duration of an event and then put together to create a still-picture movie. Last year's Steampunk OPI was also 'timelapsed' by Andrew as well:

[Watch on YouTube](https://www.youtube.com/v/auqcq5nZEvw?fs=1)

Over the course of 9 weeks, this whole party was built - you can also observe how fast clouds move, how rain .. rains, and how things seem to just 'pop-up' out of nowhere if accelerated fast enough. So without further ado (or many more words), here's a photo montage of the first two days of construction!

![](https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0147e1b13905970b.jpg)


![](https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0148c7ba7558970c.jpg)


![](https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0147e1b13ebc970b.jpg)


![](https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0148c7ba7a96970c.jpg)


![](https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0147e1b14200970b.jpg)


![](https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0147e1b1444b970b.jpg)


![](https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0147e1b14e97970b.jpg)


![](https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0147e1b156c4970b.jpg)


![](https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0147e1b15bef970b.jpg)


Join me next time when I'll talk about all things related to Stephen Hawking, including singing him 'Happy Birthday' in person! Meanwhile, Construction will still be going on - I'll update you about that, and we'll have more events at Caltech to blog about in the meantime. As always, if you have any questions or you want me to talk about something within the blog, just post a comment!

