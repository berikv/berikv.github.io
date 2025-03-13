---
layout: post
title: THE BILLIARD COMPUTER IS BACK ONLINE!
author: Berik Visschers
date: 2025-03-01 14:30:00 +0200
abstract: The micro usb port of a Biljartcomputer broke off, solder a new one on the PCB
categories: Repairs
---

## Repair Café De Bieb, Utrecht

The repair day is nearing its end, I had a lot of fun repairing [a medical device]({% post_url /repairs/2025-03-01-omron-blood-pressure-monitor %}).
What more can one ask for?

I roam around to see what repairs are in progress on the other tables when I get called over for a micro usb replacement job.

The customer shows me this device:
<img src="/assets/img/repairs/biljartcomputer/biljartcomputer.jpg" />

What. Is. That?

"A computer, for playing billiards", the customer explains.

There is an HDMI plug sticking out of the device. This must be similar to a Chromecast, but instead of displaying YouTube commercials, it tracks and shares your billiard scores!
I guess there is a community, challenging each other for competitions. Meeting IRL, and using these devices to share their match outcomes.

A whole world I didn't even know exists!

On to the repair. The micro usb port that powers the device ripped off.

That is not uncommon for usb powered devices.

One of the repairmen on De Bieb specializes in usb port replacments, they'll fix one in under 10 minutes.
This is my first usb port replacement..

Let's peek inside:
<img src="/assets/img/repairs/biljartcomputer/biljartcomputer_inside.jpg" />

An un-occupied memory slot, and a power regulator on this side. Underneeth the
heat conducting tape is a cpu and a hdmi driver.

A detail of the place where micro usb port used to be:
<img src="/assets/img/repairs/biljartcomputer/biljartcomputer_broken_usb.jpg" />

The pads that held the usb port in place have been pulled off. Other than that, the damage is minimal.
I tell the customer that this repair will succeed. They react a bit sceptical.

The five pads that look like a cross-walk ("zebra-path" in Dutch, such a great word) are [considered the usb pins](https://en.wikipedia.org/wiki/USB_3.0#PINOUTS)
while the shiny silver looking pads on top are connected to the usb shield.

The two pads that have been ripped off used to connect to the usb shield.
The fact that only these pads were ripped off tells us that the original usb port was not soldered properly.
It should have been soldered to the pads above, but it wasn't.

This usb port is for powering the device, the power is delivered over the two outermost zebra-path pads.
The second-from-the-left pad is also needed, the resistor below the zebra-path tells a charger that a
power hungry device is present. The last two pads are the data lines (up and down), and are not connected
to anything on the PCB, in this case.

This specific micro usb connector is a bit special special: the two mounting pins are a little closer together than normal.
The mounting pins fit into the oval holes in the PCB. A regular micro usb port will have them to the side of the port.
This port has them tucked underneeth, which makes soldering much much harder.

Luckily repair café De Bieb has these less-common parts on stock.

I consider the port fixed if the usb port:

* Is properly affixed
* Has the five zebra path pads connected to its leads

I could have, and maybe should have, used the hot air soldering station.

I didn't. The soldering station has to be found and set up. My regular soldering iron was ready for use.
Also, there are other ports and tiny components just near to the ripped off port. Heating up the whole area risks loosing them.

I push on, using my regular iron. Lets do this!

I use a D24 (spade shaped) tip on my T12 iron. I find this size ideal.
It manages well on pretty big amounts of copper. And with some finesse, you can work on 0.2mm jobs like these.

The repair job:

* Clear the solder from the PCB using flux, a tin sucker and wick
* Solder the matching micro usb port side lugs to the PCB
  
  Carefull here. You do not want solder to enter the usb port, like I had. If you do get solder into the usb port, do not panic.
  You can push a usb connector as far as possible into the port, take it out, heat the port until the solder inside melts, repeat.
  That should move any solder aside, until the connector fully fits into the port. Extra snug.

  Make sure to use minimal solder. Add flux with every attempt.

* Solder the usb port pins

  If you use a spade style soldering tip:

  1. Add flux. Add enough flux. Flux makes difficult soldering jobs doable
  2. Make sure a tiny layer of tin sticks to the tip of the iron
  3. Get the amount of tin right, use flux to keep the tin fluid
  4. Now, with the tinned side of the tip facing downward, press the usb pins down onto the PCB pads

     The iron tip is much bigger than the pins and pads. No worries though, if you use flux, the tin will creap between
     the metal parts and clear the places where it shouldn't be. **Do not add tin directly**, add flux intsead.

  5. Press down for 2-3 seconds until a nice sizzle starts
  6. Now pull the iron tip away from the pads and port
  7. Let the area cool a bit, then repeat until it looks decent

  I did manager to touch the voltage regulator with the soldering iron (see below).

* Lastly, Use isopropyl alcohol (IPA) with Q-tips to clean the flux from the PCB and port

  Some types of flux will damage the PCB traces and components over time, if it is left uncleaned

The new port soldered:
<img src="/assets/img/repairs/biljartcomputer/biljartcomputer_soldered.jpg" />

Once the device is assembled, we walk to a presentation display and plug the biljartcomputer into the HDMI port; then plug a usb adapter in the repaired usb connector.

THE BILLIARD COMPUTER IS BACK ONLINE!

We don't have a billiard table nearby, would have been nice to see the device in action!
