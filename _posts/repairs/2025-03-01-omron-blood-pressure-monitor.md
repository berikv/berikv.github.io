---
layout: post
title: Omron Blood Pressure Monitor Start / Stop button
author: Berik Visschers
date: 2025-03-01 13:30:00 +0200
abstract: Omron Blood Pressure Monitor Start / Stop button, open up and micro switch replacement.
categories: Repairs
---

<img src="/assets/img/repairs/omron_blood_pressure/omron.jpg" />

What a treat, a medical device!

The story of what is broken is not very clear. The repair was sent my way from another table, and I probably missed some communication. The only thing I get to hear is "Does not work!".

Well... The display clearly does something when batteries are inserted. Maybe the batteries are dead?

Measuring them, they look fine. Nonetheless, I grab a lab PSU and feed the device 6V over the battery terminals.

Not much changes. The display shows historical measurements, but the customer insist that the device does not work.
Pressing the Start/Stop button does not start the measurement procedure, which, apparently, should start the measurement.
I somehow get in the date and time setting mode, without knowing how I got there. Worse, I can't seem to exit the date and time setting mode.

Lets first try to learn a bit more about the device.
I read the [Omron M3 online manual](https://www.bloeddrukmeterswebshop.nl/media/handleiding/Omron-m3-2014.pdf) in the hope to find some clues there.
Alas, the manual does not even mention the date and time setting mode. There is also no overview of functions and how to activate them; Bummer.

Enough with the speculation and studying, lets open her up!

First remove two screws here:
<img src="/assets/img/repairs/omron_blood_pressure/omron_bottom.jpg" />

Then remove the front panel by lifting it with a spudger, undoing the plastic tabs:
<img src="/assets/img/repairs/omron_blood_pressure/omron_inside_top.jpg" />

Removing the inside from the casing is still a challenge. There are two steps:
<img src="/assets/img/repairs/omron_blood_pressure/omron_remove_innards.jpg" />

1. You must first remove the screw just below the LED indicator PCB
2. Next you lift the two plastic tabs that fix the battery container to the outer casing.

   From the back, push the battery container to the front and out while lifting the tabs on the inside, so that the container can slide freely.

Then the intestines come lose:
<img src="/assets/img/repairs/omron_blood_pressure/omron_innards_front.jpg" />
<img src="/assets/img/repairs/omron_blood_pressure/omron_innards_side.jpg" />

Beauty, both simple and complex at the same time. On the inside there are 4 PCBs!

Their functions:

* LED indicators
* Buttons
* Motor and battery connection
* MCU / Motor driver / Brains of the operation

<img src="/assets/img/repairs/omron_blood_pressure/omron_mcu.jpg" />

The components clearly have been fitted by high end 3D design software.

Much of the space inside the device is occupied by support for the buttons, display and indicators.
A core feature of this product is accessibility: There are big letters on the display, bright indicators and big buttons.

Once the device is open, I quickly determined the issue and cause.

The Start / Stop button micro-switch does not make a clickity sound when pressed. The other switches do.
Testing with continuity mode on the multi meter, my hypothesis is proven: The Start / Stop micro switch is pushed one too many times.

We have a set of 6x6mm microswitches on stock.

The repair:

* Snipped out the broken micro switch
* Cleared the PCB holes of old solder and snipped pins
* Picked a micro switch from the set that looked right
* Soldered the new micro switch in place

<img src="/assets/img/repairs/omron_blood_pressure/omron_replacement_switch.jpg" />

Testing the new switch, it works flawlessly. Time to assemble.

Everything in its place, the Start / Stop button does not work again.

SW1, the replaced microswitch, as you can see on the above picture, is just a bit taller than the other switches.

One could redo the whole operation and mount a better fitting micro switch there. But lets not waste time now.

<img src="/assets/img/repairs/omron_blood_pressure/omron_button_trim.jpg" />
I trim the button lever from the bottom side, so that the taller micro switch has room to extend.

After assembly, the blood pressure measurement device "works"!
