---
layout: post
title: Biljartcomputer micro usb port
author: Berik Visschers
date: 2025-03-01 14:30:00 +0200
abstract: The micro usb port of a Biljartcomputer broke off, solder a new one on the PCB
categories: Repairs
---

The repair day is nearing its end, and I had a lot of fun repairing [a medical device]({% post_url /repairs/2025-03-01-omron-blood-pressure-monitor %}).
What more can one ask for?

I roam around to see what repairs are in progress on the other tables, when I get called over for a micro usb replacement job.

The customer shows me this device:
<img src="/assets/img/repairs/biljartcomputer/biljartcomputer.jpg" />

What. Is. That?

"A computer, for playing billiards", the customer explains.

I see the HDMI plug. This must be similar to a Chromecast, but instead of displaying YouTube commercials, it tracks and shares your billiard scores!
I guess there is a community using these devices, challenging each other for competitions. Meeting IRL, and using these devices to share the match outcome.

A whole world I didn't even know exists!

On to the repair. The micro usb port that powers the device was ripped off.

Nothing uncommon here..

Normally one of our other repairman takes the broken usb ports. They are the expert and can repair 5 in an hour if needed.

For me, this is the first one. Let's peek inside:
<img src="/assets/img/repairs/biljartcomputer/biljartcomputer_inside.jpg" />

An un-occupied memory slot, and a power regulator on this side. On the other side
there is a cpu and hdmi driver and memory, as expected.

The place where a micro usb port need to be:
<img src="/assets/img/repairs/biljartcomputer/biljartcomputer_broken_usb.jpg" />

Some part of the traces has been ripped off. But nothing major.

The power comes in over the outer-two pins of the five that look like a cross-walk ("zebra path" in Dutch, I like it when a word discribes the visual, not the function).

This replacement micro usb port needs two things:

* To be properly affixed
* To have the five zebra path pads connected to its leads

I could have, and maybe should have used the hot air soldering station.

I didn't. The device had to be found and set up, and my regular soldering iron was ready for use.

Lets do this!

This specific micro usb connector had to be a special one, with the pins being a bit closer together than normal.

Luckily repair café De Bieb has these less-common parts on stock as well.

Looking at the picture, you might think that it's an easy job, soldering this with a regular iron.

I use a D24 (spade shaped) tip on my T12 iron. I find this size ideal. It manages on pretty big amounts of copper, and with some finesse, can also work on 0.2mm jobs like these.

The repair:

* Clear the solder from the PCB using flux, a tin sucker and wick
* Select the matching micro usb port from the set
* Solder the usb port side lugs to the PCB
  
  Carefull here. You do not want solder to enter the usb port. If you do get solder into the usb port, do not panic.
  You can push a usb connector as far as possible into the port, take it out, heat the port until the solder inside melts, repeat.
  That should move any solder slowly aside, until the connector fully fits into the port. Extra snug.

* Solder the usb port pins

  If you use a spade style soldering tip:

  1. Add flux. Add enough flux. Flux makes difficult soldering jobs doable
  2. Make sure a bit of tin is on the iron tip
  3. Make sure there is flux on the iron tip
  4. Now press down on the usb pins and PCB pads. Make sure the tinned side of the tip is facing down
  5. Press for 2-3 seconds until a nice sizzle starts
  6. Now pull the iron tip away from the pads and port

  An extra difficulty on this PCB: Within 0.5mm of the usb port pads there is a tiny resistor and just behind that, the big voltage regulator.
  It is all pretty camped.

  Using a hot-air soldering station generally is better for mounting usb ports. But in this case, with the components so close by,
  a hot-air station would have been a much more blunt tool.

  Though, I can not deny having touched the regulator with the soldering iron.

* Lastly, Use isopropyl alcohol (IPA) with Q-tips to clean the flux from the PCB and port

  Some types of flux will damage the PCB traces and components over time, if it is left uncleaned

The new port soldered:
<img src="/assets/img/repairs/biljartcomputer/biljartcomputer_soldered.jpg" />

Once the device is assembled, we walk to a presentation display and plug the biljartcomputer into the HDMI port; then plug a usb adapter in the repaired usb connector.

BILLIARD COMPUTER MACHINE BACK ONLINE!

We don't have a billiard table nearby, would have been nice to see the device in action!
