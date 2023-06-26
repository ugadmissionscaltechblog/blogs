---
title: DDR Mat Diagnostics
image: /wp-content/uploads/old_images/caltech_as_it_happens/6a0105349b8251970b01901ec2619b970b.png
date: 2013-08-19
categories: 21656
author: Laura
---

Over the summer, we've been setting up Dance Dance Revolution every Friday and Sunday night. During the school year, we usually only play on Friday nights, but since no one has any homework or sets over the weekend in the summer, we've added Sunday nights as well. Last Sunday was the first day we tested our [homemade DDR mat](https://caltech.typepad.com/caltech_as_it_happens/2013/08/first-ddr-mat-almost-done.html) extensively.

Summary: It works quite well! Unfortunately, it doesn't work quite as well as we had hoped, though it works better than the several-years-old Cobalt Flux mats we have.

Details: We had to do a lot of adjusting to get the screws in the sensors at exactly the right height. ([Here](https://caltech.typepad.com/caltech_as_it_happens/2013/07/ddr-mat-sensor-testing.html)'s my post about the sensor design.) If the screws were drilled in too far, the arrow wouldn't register all the time. But if they weren't drilled in far enough, the arrow would register randomly even when not pressed. Generally, there was only one or so "pad miss" (when the DDR pad doesn't register an arrow press properly) for every 100 or so arrows, which isn't too bad, though it does mess up attempts at full combos, which is when you hit every single arrow in a song. Hopefully we can reduce the number of pad misses even more by adjusting the height of the screws.

Sensor v1

It was difficult to make sure all the screws were at the same height, so for the second DDR mat we're building, we're going to modify the sensor design a little. Instead of drilling into the foam weatherstripping, we'll cut gaps in the weatherstripping, and then drill the screws in, using washers or spacers to adjust the height. Once we find the correct number of washers or spacers to use, it will be very easy to make sure all the screws are at the same height. The changes were inspired by the [Matrix Sensor design](https://members.shaw.ca/lluk/ddrpad/). 


![](/old_images/caltech_as_it_happens/6a0105349b8251970b019104b84974970c.png)

Sensor v2, with washers


![](/old_images/caltech_as_it_happens/6a0105349b8251970b019104c5f8c8970c.jpg)

Sensor v2 prototype

We also probably need to recalibrate the software we use to play DDR on a computer. The new DDR mat tends to register just a little earlier than the old DDR mats, most likely because the sensors are different. Fortunately, there's an option in the DDR software intended to calibrate the sound and arrows to account for input delay. Once we work out most of the kinks with the new DDR mats, we should start seeing a very low number of pad misses, and also better scores!


![](/old_images/caltech_as_it_happens/6a0105349b8251970b0192ac9661ad970d.jpg)

Grace playing on the new DDR mat

