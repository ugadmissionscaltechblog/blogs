---
layout: post
author: Laura
image: https://ug-admissions-caltech-blog-dev.s3-us-west-1.amazonaws.com/old_pictures/caltech_as_it_happens/6a0105349b8251970b01901d8b1589970b.png
title: Knots, Programming, and SURF 
categories: [research]
status: Publish
date: 2013-06-20
---


This summer I'm doing my first SURF! It's a math SURF, and my mentor studies low dimensonal topology, specifically<a href="https://en.wikipedia.org/wiki/Floer_homology#Heegaard_Floer_homology" target="_blank">Heegaard Floer homology</a>.

 I'm working on the SURF with another undergrad, so we'll be working 
together to complete different parts of the project. Our main project is to write a 
program to compute Heegaard Floer correction terms from a variety of 
input methods. For the first few weeks, I'll be working on several of 
the input methods, including getting input from a drawing of a link.

For basic knot theory, here are some useful links: <a href="https://www.oglethorpe.edu/faculty/j_nardo/knots/intro.htm#num1" target="_blank">knots</a> <a href="https://en.wikipedia.org/wiki/Link_%28knot_theory%29" target="_blank">links</a> <a href="https://planetmath.org/alternatingknot" target="_blank">alternating knots</a> <a href="https://www.math.cuhk.edu.hk/publect/lecture4/alternating.html" target="_blank">more alternating knots</a>

A quick summary: A knot in math is basically the kind of 
knot you tie, except that the ends of the knot are connected so there's 
no loose ends. Here's a picture of a trefoil knot:

<div class="photo-caption caption-xid-6a0105349b8251970b01901d8b1589970b" id="caption-xid-6a0105349b8251970b01901d8b1589970b">Trefoil knot drawn by Knotilus

A link is what you get when you have multiple knots linked together, like the Borromean rings here:
<div id="photo-xid-6a0105349b8251970b019103813347970c" style="display: inline-block; width: 320px;">


{% include image.html img="https://ug-admissions-caltech-blog-dev.s3-us-west-1.amazonaws.com/old_pictures/caltech_as_it_happens/6a0105349b8251970b019103813347970c.png" %}<div class="photo-caption caption-xid-6a0105349b8251970b019103813347970c" id="caption-xid-6a0105349b8251970b019103813347970c">Borromean rings drawn by Knotilus

An
 alternating link is a link with a diagram such that if you start 
anywhere on the link and follow the strand you're on, the crossings 
alternate over, under, over, under, etc. or under, over, under, over, 
etc. The trefoil knot and Borromean rings are both alternating.

----

One input method for my SURF project is to take an alternating link 
projection, shade regions of the link, and then use the shaded regions 
and intersections to create a graph (the kind with nodes and edges). For
 example, the program <a href="https://www.math.uic.edu/t3m/SnapPy/plink.html" target="_self">Plink</a>
 lets a person draw a link with their mouse. Part of the algorithm is 
then to load the drawing and shade regions (while keeping track of 
them), like in the picture below.


{% include image.html img="https://ug-admissions-caltech-blog-dev.s3-us-west-1.amazonaws.com/old_pictures/caltech_as_it_happens/6a0105349b8251970b0191038144dd970c.png" %}<div class="photo-caption caption-xid-6a0105349b8251970b0191038144dd970c" id="caption-xid-6a0105349b8251970b0191038144dd970c">Link drawn in Plink (left) and shaded regions (right)

Based on the shaded regions and intersections, a graph and quadratic form can be calculated for each link projection. The quadratic form can then be used to calculate the Heegaard Floer correction terms.

Since I'm doing a math SURF, I don't have to go to a lab or anywhere specific on campus to work on the project. Although the view from my dorm room is very nice, it can get lonely in the morning since most people are at labs or JPL. So for the first day, I decided to go work in Annenberg (the computer science building), since they have an undergraduate computer lab. 

{% include image.html img="https://ug-admissions-caltech-blog-dev.s3-us-west-1.amazonaws.com/old_pictures/caltech_as_it_happens/6a0105349b8251970b0191038189d5970c.jpg" %}<div class="photo-caption caption-xid-6a0105349b8251970b0191038189d5970c" id="caption-xid-6a0105349b8251970b0191038189d5970c">View from my summer dorm room (the blurriness is from the window screen)

For some of the other inputing methods for the SURF project, I'll first have to learn more about 
topology and read a little about homology. My list of topics to learn about include plumbed 3-manifolds, Seifert fibered rational 
homology spheres, and Dehn surgery. Fortunately I know several other math majors staying at Caltech over the summer!

