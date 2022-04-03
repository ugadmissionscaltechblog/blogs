---
layout: post
author: Laura
image: https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b019103b6fe3e970c.png
title: The Knotilus Database 
categories: [research]
status: Publish
date: 2013-06-28
---


<a href="https://knotilus.math.uwo.ca/" target="_blank">Knotilus</a> is a database of all prime alternating links with 23 crossings or less (according to their website there are 98,517,495,461 such links). It's great for browsing pretty pictures of knots and links (with different colors!). Along with pictures of the links, Knotilus provides its own archive number, the Gauss code for the alternating link, other knot tabulation numbers, and information about the symmetry and orientation of the link. The Knotilus archive number is of the form ax-b-c, where a = number of crossings, b = number of link components, and c = the cth link in the archive for a set a,b. For example, 6x-1-1 is a knot with 6 crossings and 1 link component (hence a knot), and is (arbitrarily) the first knot listed in the archive with those properties.

One input method for my SURF project is inputting the Knotilus archive number, so my script needs to download the corresponding plaintext file from the database. Last week, one of my friends showed me how to view network requests on Chromium or Chrome (right-click on page &gt; Inspect Element &gt; Network). After viewing the network request while downloading the plaintext file for a knot, Chromium recorded the URL to directly download the plaintext file. Viewing network requests also gave me the URL for the page that loads the knots. Some knots/links with a higher number of crossings take several seconds (up to 15 or so) to load or "anneal", and requesting the plaintext file before the knot has loaded produces an empty file. As a result, my program has to keep requesting that different URL to load the knot until the plaintext file is non-empty.

 One of the main things I'm working on is adapting the previous code I wrote for Plink to work with the Knotilus downloads, since the information given by Knotilus is different than the information given by Plink. Currently I'm working on minimizing copy-pasted code, and making functions handle input from both Knotilus and Plink correctly.

To prepare to calculate the Heegaard Floer correction terms, knots/links from Knotilus and Plink first need to be loaded, and then shaded according to a convention in a <a href="https://arxiv.org/abs/math/0309170" target="_blank">paper</a> by Ozsvath and Szabo. That paper is actually the paper with the theorem for Heegaard Floer correction terms, published recently in 2003. (Heegaard Floer homology is a recent and current area of math research!) For the shading convention, you take the knot, look at an intersection, and shade the knot according to the picture below. While this is pretty easy to do by hand, it's a bit harder to tell the computer which lines to color inside! The overall method for Knotilus/Plink links looks something like: 

Input -&gt; double branched cover of alternating link -&gt; quadratic form (matrix) -&gt; (use algorithm and theorem by Ozsvath and Szabo) -&gt; Heegaard Floer correction terms
<div class="photo-caption caption-xid-6a0105349b8251970b019103b6fe3e970c" id="caption-xid-6a0105349b8251970b019103b6fe3e970c">Shading convention from the paper by Ozsvath and Szabo


{% include image.html img="https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0192ab7dd495970d.png" %}<div class="photo-caption caption-xid-6a0105349b8251970b0192ab7dd495970d" id="caption-xid-6a0105349b8251970b0192ab7dd495970d">Several links from Knotilus, after downloading and running through my program.

If you're interested in what those links actually look like without the shading and straight edges, you can look them up in the Knotilus database. The Knotilus archive numbers are (top to bottom, left to right), 10x-1-10, 11x-1-1, 14x-1-1, 23x-1-1, 23x-1-2, 23x-2-1, 23x-2-10, 23x-10-3, 23x-11-1. My program draws the links upside down because of the way that Tkinter (GUI package for Python) sets up its coordinate axis; the positive y-axis points down.

Next input method: Seifert fibered rational homology spheres and weighted trees!

