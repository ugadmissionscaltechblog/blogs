---
layout: post
author: Casey Carter Glick
image: https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0133f26e19a2970b.jpg
title: Introduction to Microfluidics 
categories: [research]
status: Publish
date: 2010-07-21
---


Current Music: Beethoven’s 9<sup>th</sup> Symphony and Verdi Requiem

Current Foods: Cherries, Cherry Tomatoes, and Black Tea

Hi again,

The question that most desperately needs answering at this point seems to be: why is a Caltech applied physics major doing microfluidics research at Stanford this summer? The answer to that question will be the topic of this post as a segue into my current work here at Stanford (which will be described later). It is a little heavy on background and technical details, so bear with me, and feel free to ask for clarification in the comments.

During my sophomore year (over a year ago), I decided I wanted to do a <a href="https://www.admissions.caltech.edu/learning/research">SURF</a> (Summer Undergraduate Research Fellowship) abroad. One of my favorite features of SURF program at Caltech is that it allows us to work at pretty much any institution we want, so long as we can find a mentor interested in working with us. For the most part, SURFs away from Caltech are arranged like any other SURF; prior arrangements with a mentor are required to receive the fellowship. However, Caltech also offers a few special foreign exchange SURFs: to Iceland, Hong Kong, India, and Singapore, plus France, where students apply to the program, and find a mentor once accepted to study abroad. I applied to the program for both Iceland and Hong Kong, and was awarded the SURF for Hong Kong. (I was the only student to apply for the Hong Kong program, so I recommend that anybody interested should definitely apply when the time comes!) I found a professor, Weijia Wen, with whom I wanted to work, and he accepted me into his lab for the summer.

Picture: me holding two firedragon fruits at HKUST

Professor Wen’s “Smart Materials Lab” specializes in both microfluidics (the study of fluid flow in very small channels) and electrorheological (ER) fluid (a type of liquid that changes its viscosity depending on the voltage applied to it). I had thought I wanted to work with ER fluid from a chemical perspective, but I discovered that he was doing something even better in his lab; he and his grad students were working on ER as a precision control mechanism for microfluidic devices.

Microfluidics is a relatively new field that has developed greatly in the last ten years. The point of microfluidic research is to create functional Labs on Chips, functional biological or chemical laboratories that fit in the palm of your hand, and require only nanoliters of chemicals to run. Already, devices exist that cut the time required to perform PCR (polymerase chain reaction, a process to replicate DNA) by 66%. Yet these chips are inefficient, hard to control, and difficult to use, due to the fundamental problem of microfluidics: it’s hard to control fluids in 100 micrometer (and smaller) channels! The rules that govern the movement of fluids at large scales just don’t apply in the microfluidic realm; whereas on human scales, the inertia of the fluid is a driving force for fluidic movement (think of the wake of a motorboat or the turbulence of a river), at small scales, the viscous force dominates. For a good description of the difference between the macro and the micro fluidic worlds, read Purcell’s lecture “Life at Low Reynolds Number”

<a href="<https://jila.colorado.edu/perkinsgroup/Purcell_life_at_low_reynolds_number.pdf>">https://jila.colorado.edu/perkinsgroup/Purcell_life_at_low_reynolds_number.pdf</a>

(Purcell is near and dear to the heart of many Caltech students; his textbook is required for the Physics 1b and 1c analytical track, and is one of the best Electricity and Magnetism “introductory” textbooks out there.) In short, if you want to control a microfluidic device, you have to come up with completely new control mechanisms to do so. The techniques worked out for macrofluidics for making transistors, diodes, inductors, etc. will fail in microfluidics; very little that works at large scales still applies when you make a device small.

There are a handful of good solutions to this problem that are currently under development, and two major ways of thinking about microfluidic flows. In general, flows can be continuous streams of fluids, or can utilize discrete droplets (“digital” microfluidics). As an example, think of water droplets suspended in oil as they travel down a channel. This view is clearly ripe for thinking of droplets as 1’s, and their absence as 0’s, thus creating a microfluidic complement for electronics circuits. The biggest difference between electronic and microfluidic circuits, though, is that the droplets in microfluidics are useful for something other than serving as a bit of information; these droplets are inherently useful, given that they can contain chemical, biological, electrical, and optical information within a single bit. Although this is a useful feature, it doesn’t mean that microfluidics will be replacing electronic circuits anytime soon (or ever); your computer will still be electricity-based for a while. So while digital microfluidics won’t turn your computer into a chemical laboratory, it CAN turn a chemical laboratory into a simple computer. At least in theory…and that’s where I come in

{% include image.html img="https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0133f26e15f6970b.jpg" %}
My work deals with control mechanisms for digital microfluidics. My lab mates in Hong Kong had already figured out how to make highly precise droplets (1’s and 0’s) using electrorheological fluid. In the following picture, they use the ER mechanism and a computer to spell out HKUST with electrorheological fluid:


{% include image.html img="https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b0133f26e179d970b.gif" %}The question I decided to solve was whether we could use the 1’s and 0’s generated by their techniques to perform logical operations. I started out by asking: can I take a signal of droplets and generate its inverse (the NOT function)? The answer turns out to be: “very yes;” not only can we make NOT gates, but also a “Universal Logic Gate” as well, a device that can perform all 16 two-input logic functions with a little reprogramming. I figured out that last one with about a week left in Hong Kong. However, by the time I got around to building it, my time at HKUST had run out (an inconvenient typhoon on my last day didn’t help), and I couldn’t test my final product. However, the mathematics work, and so did all previous designs that I managed to build correctly (I had about a 5% success rate in building my microfluidic chips).

Dr. Wen's Smart Materials Lab

{% include image.html img="https://d24slhcvzhzz82.cloudfront.net/old_images/caltech_as_it_happens/6a0105349b8251970b013485934b3f970c.jpg" %}
This is where my research was left for almost a year. Over the course of my junior year, I occasionally sketched out new ideas, but I only had vague ideas about how I was to proceed once I finished testing my universal logic gate. Even then, my logic gate is not that useful by itself (although it has dramatic potential). The gate itself is like a switch that responds to a droplet that activates in response to a droplet. What I really needed to do was figure out how to make the switch DO something; to use an electronics analogy, I HAD a switch attached to a small test bulb (to tell me whether the switch was on, or off), whereas I WANTED a switch mounted to the wall and controlling my fancy chandelier. And to do that, I knew I’d have to overcome some rather formidable technical barriers, barriers that are the focus of my summer research. To put it colorfully, I had 99 problems, but a Switch ain’t one.

Then, at the start of Spring Term, my work started to pick up pace. I had known for some time that Dr. Quake’s group was one of the few places where I could do anything useful with my project, and a helpful contact in the Caltech Technology Transfer Office, Fred Farina, put me in touch with Dr. Quake, who then accepted me into his group for the summer. Then I took Shuki Bruck’s fabulous IST 4 menu class (Menu classes are required for all Caltech students, as a way of examining areas of science we ordinarily wouldn’t explore as part of our major), where I began to study the formalities of computer logic. I’m quite lucky in this regard; the CS (Computer Science) majors figured out most of the theory needed to effectively utilize simple computer logic almost 50 years ago. I know, in general at least, what I’m supposed to be building as an end product. I just have to figure out how to get there. All it will take is building the logic gates, getting them to work effectively, physically connecting all the tubes and electronics into a device with channels smaller than 100 microns across and 10 microns high, and then extensively testing these products. Should be a piece of cake, right? At least the hard math is done…

This is where my research was when I arrived at Stanford three weeks ago. I’ve made considerable theoretical progress since then (lots of pen and pencil sketches in a couple notebooks), but I haven’t yet had a chance to start building anything. My photolithography masks just came in this afternoon, so I should be able to start working in the clean room tomorrow (yay bunny suits!) If anybody is interested, I’ll talk about some of my specific problems in a later post. As always, I welcome your comments!

-Casey
