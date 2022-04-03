---
layout: post
author: Anton Bongio Karrman
image: https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b01157234834a970b.jpg
title: Guess who's back with a brand new track...

categories: [research]
status: Publish
date: 2009-07-27
---


And here I thought that life with a 9 to 5 job could never be as busy as Tech!!! 
Maybe that's because it's uh... NOT a 9 to 5 job anymore. So my project is so close to being finished (kind of). I've basically learned everything I need to know, and written all the little parts of code I'll need, la dee da... Now it's time to streamline everything!
Here's the thing: the level set routines that I've been using are all made for a matrix mesh that is oriented a certain way... If you want a point (x,y) on the level set, you just just take the (i,j)th component of the matrix and multiply by dx,dy repsectively... Well for the finite element routines, BLEH it's made so that the rows are different y values, so to get (x,y) you have to call the (j,i)th element. And there's no sense of length associated with the finite element routine; so the analysis is dependent on making sure the mesh is discretized with an element aspect ratio of 1...  Otherwise the computation just looks.... nasty... Too bad... So it sounds easy, but it actually turns out that there are many subroutines that have been written with one context or the other, so we can't just "flip" or transpose the mesh because other things will get very sad. So that's what I'm trying to figure out right now! :)
IN OTHER NEWS :)Continuing from where I left off!
So the rest of the weekend with Sarah was incredible! On Saturday evening, her two aunts (sweetest ladies EVER!) had us over for dinner! It was great: we started off with snacks and if you recall, I mentioned earlier that aperatif is both an appetizer as well as a liquor drink... Well when they offered me an aperatif I just assumed they were talking about appetizers... But they actually offered me a drink called crema mandorla, which is an aged combo of almond extracts and Marsala wine... To be polite I drank it and it was rather sweet, so naturally I loved it! I told them I would need to memorize the name of it so I could maybe one day enjoy it again... (REMEMBER THIS LITTLE PART OF THE BLOG)...

Anyway, so for dinner we had some delicious things including about a million croque monsieurs (grilled sandwiches, the flavors we had included banana, chocolate, apple, as well as ham and cheese; OMG YUMMO). And that was the main course!!! And then for dessert we had some raspberry ice cream with fresh raspberries and whipped cream that was made from scratch (I ADORE this last ingredient, btw). Not only that, but all of us even took shots at the piano! It was so fun and I was so happy to play the piano again! One of Sarah's aunts is suffering from Parkinson's disease, but that didn't stop her NO NO she got on that piano AND ROCKED THE HOUSE WITH EVERY ELDERLY BONE IN HER BODY!!! :D
Well I had such a great time with them, I told them I would have to have a photo of us all! But I had forgot my camera :( "NO PROBLEM," said Sarah, "we can just back tomorrow." Which we did. AND YOU WILL NOT BELIEVE THIS, THEY HAD ACTUALLY BOUGHT ME A BOTTLE OF CREMA MANDORLA!!!!!! Like sweetest ladies ever? I'll never forget the delicious food, their supreme kindness, and our bouts on the piano! Wonderful! :) I will meet Sarah again just before I leave, when I will ask her to give thank you notes to the great hospitable people of Bethune :)

And then Sunday it was off to Lille! Sarah drove us for the hour long voyage, and when we arrived at her flat there suddenly she started FREAKING OUT. She had forgotten her laptop in Bethune, which held all of her work that she needed to have during the week for her physical therapy internship and university studies... Zut alors! After she had made several frantic phone calls requesting family members back in Bethune to bring the laptop to Lille, she suddenly realized that BAM, it was in the suitcase!!! Whew :D
Well to be honest, although Lille is cute and everything, nothing is open on Sunday (like most towns in France, shame...) 


{% include image.html img="https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b01157140b48e970c.jpg" %}Sarah and me in front of the Opera House of Lille...


{% include image.html img="https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b01157235490b970b.jpg" %}


{% include image.html img="https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b01157140b9b1970c.jpg" %}

{% include image.html img="https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b01157238af1b970b.jpg" %}The jazz musicians that night :)

Anyway, before I end this session, I'll just include a little story about how I got my ticket to Lille... So I found this guy selling a ticket on a site. It was $22 first class O_O rather than $39 second class, the latter I would have had to pay on the official TGV site... Anyway, I met up with the guy, got the ticket and had a cup of coffee with him and darn it, the ticket worked!!! Woohoo. It was kinda funny, he actually was an immigrant from Africa that had overstayed his carte de sejour (like a green card). This was sketchy as heck but ended up just being AWESOME ;-)
Anyway, coming up....

Tour de France, getting my new camera :), buying tickets for my ACTUAL vacation (btw I haven't had more than one work day off since Spring Break FML)... :) and trying to deal with some musicians...

You'll hear from me soon! :)
Best,
Anton

