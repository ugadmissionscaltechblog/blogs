---
layout: post
author: Laura
image: /old_images/caltech_as_it_happens/6a0105349b8251970b019aff1e3320970d.jpg
title: Soldering for DDR Mats 
categories: [global]
status: Publish
date: 2013-09-07
---

One of the last steps of building [the DDR mats](https://caltech.typepad.com/caltech_as_it_happens/2013/08/first-ddr-mat-almost-done.html) is getting a circuit board to connect a mat to a computer. One of the easiest ways is to buy a cheap USB game controller, solder wires to the contact points on the circuit board, and then connect the wires to the DDR mat.

Wires soldered to the circuit board

The steps I followed are basically:

1. Make sure the controller works when plugged into a USB port. (One of the first controllers I tried using several years ago was a PlayStation2 controller, and probably didn't work with the PlayStation2 -&gt; USB adapter I was using. But since I didn't check before opening it up, I'll never know if it just didn't work with the adapter or if I broke something while opening it.)
2. Test in whatever DDR software you plan to use - make sure the controller can register all four arrow presses at once. If not, you might have the ["joystick axes" problem](https://www.stepmania.com/wiki/Joystick_Axes_Problem), so you'll just want to pick some other buttons to solder to. Make sure whatever buttons you choose for the four arrows can register as pressed all at the same time. This also makes hands (3 or 4 arrows pressed at the same time) possible.

3. Take out all the screws in the controller and open it up. Remove all the rubber buttons and motors if desired (just rip out the motors). 
4. Use an Ohm-meter to figure out which solder points are ground. Each button will generally have two solder points near it, one of which is ground. If you touch two solder points for different buttons, and the resistance is very close to zero, chances are that those solder points are connected to ground. Sometimes the entire controller will only have a single ground (which is very convenient), but sometimes each section of the controller will have its own ground.

5. Solder one wire to the easiest to reach ground solder point. (Repeat this step if your controller has multiple sections with different ground.)
6. For each button you want to use, solder one wire to the non-ground solder point.

7. Group the wires neatly, put some electrical tape on the circuit board, close up the controller, and test it again on the computer. Go back to step 4 if it doesn't work.

8. Connect the wires to the DDR mat. In this case, that meant soldering to a male D-sub connector (HD15, same as a VGA cable), since our DDR mat wires are soldered neatly to a female D-sub connector.


![](/old_images/caltech_as_it_happens/6a0105349b8251970b019aff1db351970b.jpg)

Wires from circuit board soldered to a D-sub connector

Tips: The wires are often easier to position if you can find (or drill) a hole near each solder point. Then you can poke the wire in from the back and fold it over onto the solder point. For soldering, lead solder usually sticks better than lead-free solder (unfortunately). It works pretty well to put a small glob of solder on each solder point, then remelt it and shove the wire into the solder.

As for [the DDR mat](https://caltech.typepad.com/caltech_as_it_happens/2013/08/ddr-mat-diagnostics.html) itself, it turns out the weatherstripping foam we used is too soft and compresses too easily after a few hours of playing DDR. So we'll probably try different kinds of foam or rubber until we find one that keeps its shape well after compression. (Current ideas are mousepads or cheap flip flops!)
