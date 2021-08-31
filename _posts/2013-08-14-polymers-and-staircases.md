---
layout: post
author: Kiara
image: https://ug-admissions-caltech-blog-dev.s3-us-west-1.amazonaws.com/old_pictures/caltech_as_it_happens/6a0105349b8251970b0192ac79564c970d.jpg
title: Polymers... and Staircases?
categories: [research]
status: Publish
date: 2013-08-14
---


Hi everyone, it's been a while, I know. Japan has been a very busy (and fun!) time - work during the weekdays takes up quite a bit of energy, and the rest has been used up going to various places during the weekends. Since the work has been winding down a bit, I suppose now's a good time for me to talk about it. :)

My work this summer focuses on properties of polymers, particularly the property called the glass transition temperature (Tg). The glass transition temperature is when an amorphous polymer goes from being hard and brittle to being rubber-like. Polymers are special in that they can be arranged in two ways: amorphous (no defined shape) or crystalline (well-ordered, has a defined pattern). When I was first reading up on this, one source I found said to think of crystalline as uncooked spaghetti in the box and amorphous as cooked spaghetti. That might be an oversimplified way of thinking about it, but it helped me a lot at first. One polymer chain could also be semi-crystalline (both amorphous and crystalline) - since Tg is associated with amorphous polymers, I did not have to work with that this summer.

Speaking of working with polymers... I'm in the computational materials science team, so I create these polymers on the computer. For this, the company uses a program that we'll refer to as MS. It's probably a good idea for me to not be *too* specific... Anyhow. The process of my work basically involves using MS to create the polymer and make it amorphous, export it to another program we'll call MA (which I have my quips about), use MA to change the force fields and get input files for that are compatible with LAMMPS, the molecular dynamics simulation program I use (it's open-source, so it won't hurt to actually name it), run the LAMMPS simulation, keep myself occupied with something else (because simulations take at least 2 days to finish), and then go back to MS to analyze the molecule's movement over time. Doesn't sound too difficult, right?

The thing about research is that you are bound to run into some strange problems. One of the first problems I encountered was that MA was making my molecule look really strange. The first time I went through the simulation process and opened the animation file on MS, I was not expecting this at all:
<div class="photo-caption caption-xid-6a0105349b8251970b0192ac79564c970d" id="caption-xid-6a0105349b8251970b0192ac79564c970d">You probably weren't expecting that either.

To figure out the cause of the problem, one of the people in the team I'm in did the same process on his computer, with the same version of programs, with the same operating system... His was fine. It turned out that my version of MA was changing the boundary conditions, while his wasn't. We found a point of difference eventually...

...His program was in Japanese; mine was in English. Who knew that could be so problematic?

While we couldn't do much about MA being a source of annoyance, we found a way for MS to display it nicely, so it turned out fine in the end. Through my internship, I've gone through this proces numerous times - with different polymers, different numbers of chains, and different force fields; it's been fascinating to see the differences that could happen by changing one parameter.

Now, a bit about work life:

Despite doing a similar type of work as I did for SURF after my freshman year, one of the main differences between then and now is that at a company, you don't really get to choose your work hours. Even though one of my seniors claims that the company I work for has flex-time (i.e., you can come in as early/late as you want as long as you work at least 8 hours), that doesn't apply to me, and I don't think flex-time exists for most Japanese companies either. Since work is nowhere near walking distance and I don't have a car, I have to take the company bus... Which arrives in the dormitory at 7:36 AM, give or take a few minutes.

As someone who has managed to completely avoid lab sections that start at 8 AM during my time at Tech so far, that took a while to sink in. During the first few days, I still had some jetlag so I'd wake up at 4 AM, so being ready on time was not a problem at all, but once my sleeping schedule adjusted to the timezone... *Well.* There have been a couple of times when I missed the bus - the first time was particularly stressful, since I reached the lobby and witnessed it zoom off and had no idea what to do afterwards. Thankfully, one of the girls in my dormitory floor who had a car had not left yet and didn't mind taking me along with her, so crisis averted!

At work, we wear uniforms, so when people arrive, they go to the locker room to change first before heading off to the workplace. One particular staircase is closest to the locker rooms, and having climbed it multiple times, I couldn't help but take note of the things that are written on it. The things written are what you'd expect, such as "Hold on to the railing" (another staircase that doesn't have things written on it has a radio attached to the wall telling you the same thing when you pass it), but there was one that really caught my attention:

{% include image.html img="https://ug-admissions-caltech-blog-dev.s3-us-west-1.amazonaws.com/old_pictures/caltech_as_it_happens/6a0105349b8251970b01901eba2788970b.jpg" %}<div class="photo-caption caption-xid-6a0105349b8251970b01901eba2788970b" id="caption-xid-6a0105349b8251970b01901eba2788970b">I'm referring to the top one.

To y'all who can't read Japanese, the top one says "No poketto hando! (Don't put your hands in your pockets)" While it did a good job of catching my attention, I didn't notice the things in parenthesis during the first few times and I was *really* confused. I understood it after I read the things in the parenthesis. Strange.

There's definitely a lot of other work-related things I can talk about, but that'll have to wait for another time. Stay tuned!

