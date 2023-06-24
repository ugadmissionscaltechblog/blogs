---
layout: post
author: Anton Bongio Karrman
image: https://d24slhcvzhzz82.cloudfront.net/old_images/6a0105349b8251970b0120a4ea8eb1970b-800wi.jpg
title: IT'S ALIVE.  IT'S ALIIIIIVE!
categories: [research]
status: Publish
date: 2009-08-12
---

My code is working. My code is working. AWESOME.

Before I discuss this AWESOMENESS, I will first recount my last week or so in and near the "city of lights."
So where to begin... I got a new camera (as in I exchanged the old one for this new one)! :D Looks like I'll actually keep this one, too! And please if you're a pickpocket in Paris, don't steal this one! But because of my glorious experience with having my last one insured, I am most definitely going to get this little bugger insured as well.

That was Saturday. The next day there was little a bike race in town. You might have heard of it, it's called the [Tour de France](https://en.wikipedia.org/wiki/Tour_de_France), and the cyclists are incredibly fit people representing teams and countries from all over the world . They bike all over France and a bit in Spain; it's really amazing how huge the mountains they tackle are! Anyway, I found a really cool place to stand near the street, so I had the opportunity to see the "parade" fly by several times. AWESOME. I was with another international exchange student, Brendon. He just graduated from Princeton with a physics degree o_0 and liked the uni so much that he's going back there for more at grad school! Anyway, we were going to try to meet up with others, but it was a madhouse near the finish at the [Champs Elysees](https://en.wikipedia.org/wiki/Champs_Elysee). 
We ended up just getting some delicious sandwiches and checking out the exterior of the Louvre, which is one of the most famous museums in Paris and maybe even in the world... I have been to see its art once before and of course saw the Mona Lisa, but that was 5 years ago, so I might choose a Sunday, when supposedly you can get in for free, to check it out again!
Monday it was back to work again! However, Tuesday we had another little picnic at Cite Universitaire as a way to say farewell to several students that are here doing research as part of a program sponsored by NSF through the University of Michigan. These guys were really great to get to know a bit throughout the weeks.

Anyway the picnic was a blast. Fun people, good food, and some extremely disturbing stories that were kind of hilarious but I would never share them on here! After we had eaten, we heard some people from the fourth story of the building next to the courtyard we were in yelling in celebration of something. So we joined their cheers and a moment later, they came to the balcony and began yelling down at us, inviting us to come up and join them. Well at first it seemed a bit sketchy, but after they insisted we merge our feasts, we could not resist.

So we tried to get into their building, which was the Belgium House (at Cite Universitaire each dorm building is named after a country from which the majority of its residents come). Well my friend Katie (a biochemist from MIT) and I looked very suspicious trying to get into the building by waiting for someone to exit and just "happen to" hold the door open for us. Thankfully tho, some of our crew had already made it up before we had, so they asked the host of the little soiree to come downstairs to welcome us, which is how we met Serge. Very friendly, nice, and good host! haha

![](https://d24slhcvzhzz82.cloudfront.net/old_images/6a0105349b8251970b0120a541bbba970c-800wi.jpg)Anyway, he invited us up where we met with the others that we already knew as well as some people from la Maison de Belgique (Belgium House). There was a freaking UTOPIA of food in that kitchen! Luca, from Italy, made like several fresh pizzas for us, there were several different beverages to which we added slices of delicious strawberries (as a joke, I was allowed 2 slices ONLY in each drink; if I put more than 2 in, it was against tradition ;) Then they had two different types of cake for dessert. It was incredible. Everyone we met was extremely nice and geez they shared all that stuff with complete strangers (us)!
So why don't I talk a bit about my project. The past few weeks have been hell because I basically had figured out everything for the shape optimization algorithm except how to exactly calculate the velocity field with which I needed to advect the level set equation. I had my entire algorithm written in Scilab and I kept TESTING AND TESTING AND TESTING and never had any luck getting the right velocity field. When I would apply it to my initialized mesh, the mesh would blow up or do something else really stupid, which was pointless because the whole point of this vector field is that if you use it (the correct one at least) then the compliance is minimized. The compliance is the total work that the forces acting on the structure do (on a microscale so that we can use linear approximations for the elasticity equations). This means that you're getting a structure that is not deforming that much when you apply a force, and if it's not deforming that much, it means it is (in common terms) strong and rigid.

So finally I figured out how to get the right velocity field! And deliciously optimal structures are materializing from initialized meshes! I honestly thought for a long time that I would not get to this point and thus would have nothing to show my mentor, but I was wrong! 
Check out my progress :)
[https://www.cs.caltech.edu/karrman/Doc1.htm](https://www.cs.caltech.edu/%7Ekarrman/Doc1.htm)
I'll write about more stories soon!
Always,Anton
