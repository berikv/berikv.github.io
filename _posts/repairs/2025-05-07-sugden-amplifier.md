---
layout: post
title: "Sugden A25 - Professional Repair"
author: Berik
date: 2025-05-07 12:00:00 +0200
abstract: Capacitor replacement and new knobs for the Sugden A25
categories: Repairs
---

## Professional Repair

A repairman asked me to repair his Sugden A25 amplifier. What an honour!

The machine works, but there is an audible 50Hz tone coming from the speakers. I immediately conclude that this must be the rectifier capacitors.

After receiving the machine and opening it up, there is a clear visual confirmation:
<img src="/assets/img/repairs/sugden_a25/06E4BA5D-E48B-404F-9BA7-ED197DA171A9_1_105_c.jpeg" />

Both capacitors have formed a slight bulge due to internal pressure buildup.

I remove both, and they measure 1000x less than their rated value. Due to the way they are laid out on the PCB, and the height of the machine, I need to order the exact size: 35mm by 20mm, 10mm lead spacing. These are Rubycon branded capacitors — Sugden did select quality components! I can only order a batch of 500 Rubycons of the correct value and size. I check in with the customer to see if they mind another brand. I get a reply of full confidence in my expertise and go ahead with the repair.

Let’s be diligent, now that I’ve received full confidence. I inspect each component on the PCB and see some interesting features.

<img src="/assets/img/repairs/sugden_a25/DFCBE419-7B73-4E8A-8463-70F2D2EECCE7_1_105_c.jpeg" />
<img src="/assets/img/repairs/sugden_a25/A366D98F-8BA2-4872-94EC-5225AA1DD436_1_105_c.jpeg" />

Three things to notice here:

- The PCB seems to have been bent along the power transistor legs  
- The PCB shows some slight discoloration around the transistors  
- The ceramic capacitors have developed a white, stubbly beard  

I first deal with the capacitors. For each type, I desolder one or two and measure their value out of circuit. Quite a few capacitors are out of spec:
<img src="/assets/img/repairs/sugden_a25/C1294DC2-A971-48AF-8D16-717EAC0BC43A_1_105_c.jpeg" />

The two big ones are the rectifier capacitors that failed completely. The others still have some value, but less than specified (whatever it says on the outside ±20%, for most capacitors). Also, ideally, if there are four capacitors with the same specified value, you wouldn’t want to see one being +20% and another being -20%.

I leave the capacitors that measure fine — they've survived over 40 years, and chances are good they’ll survive another 40. For the out-of-spec capacitors in the photo, I order replacements.

There isn’t much point in testing the amplifier without having good capacitors in place. Instead, I do some work on the front panel.
<img src="/assets/img/repairs/sugden_a25/AD626992-F186-4CEB-BAAA-A35DF43F41D6_1_102_o.jpeg" />

One of the knobs is missing, and another is split in two.

I ask a friend with a 3D printer if they fancy printing a knob.
<img src="/assets/img/repairs/sugden_a25/A5924D2B-890C-4FAF-A1AF-22F52BDED6ED_1_105_c.jpeg" />

I measure and sketch the knob specifications, then visit my friend with this piece of paper. About an hour later, we have the first attempt printed.
<img src="/assets/img/repairs/sugden_a25/052EBB59-468A-457B-A508-5311E9CB059F_1_102_o.jpeg" />

In the photo above, the original knob is on the left, and the printed knob is on the right. I ask my friend if the inset can be printed as well. The next day, they deliver:
<img src="/assets/img/repairs/sugden_a25/C3B08F01-BC64-444D-BDFC-AAC035086574_1_105_c.jpeg" />

I spend 10 minutes per knob flattening the print lines, then sanding, then painting.
<img src="/assets/img/repairs/sugden_a25/DBDF2207-D0B3-42C6-AA77-FBDDCC127455_4_5005_c.jpeg" />

One gets a different treatment. Being printed in red, I add a few layers of red spray paint with a nice gloss.
<img src="/assets/img/repairs/sugden_a25/728F99A1-C5CC-45A7-BE14-8B9144B23DE3_1_102_o.jpeg" />

I'm proud of the result:
<img src="/assets/img/repairs/sugden_a25/43D713BD-6054-41CF-A7AA-EC3AE0B78C6C_1_105_c.jpeg" />
<img src="/assets/img/repairs/sugden_a25/CDF1085A-D216-44C5-BBB9-BD44AAACD2CE_1_105_c.jpeg" />

I fix the knobs in place with some silicone glue. This type of glue does not become fully hard, so the buttons can be replaced later if needed.

I show the result to the customer: "A red button?!" he responds jokingly. I tell him he’ll receive an extra black button and can decide which one to use himself.

Once the capacitors arrive by mail, I continue with the electrical repair. With the new capacitors in place, I test the amplifier. The volume knob crackles when turned. Otherwise, the amplifier works as expected. The 50Hz hum is gone.

The PCB bend marks are not visible on the side with the traces. These are no concern. There is quite some 40 year old flux residue on the solder side of the PCB, which I clean up using some isapropanol alcohol.

I fix the volume knob using some contact spray. Spray a bit of contact spray inside the potentiometer — on the Sugden that’s the blue box right behind the volume knob — then rotate the volume knob up and down for a minute or two.

Lastly, I apply some silicone glue to the bigger electrolytic capacitors. This amplifier won’t be shaken much, but I want to deliver quality. A bit of silicone glue relieves the stress on the capacitor leads when the amplifier is moved or shaken.

Time to go the extra mile. I check the documentation for the bias current and find it should be between 80 and 100 mA. To measure the bias current, remove one of the four fuses near the power MOSFETs and replace it with a multimeter in current measurement mode.
<img src="/assets/img/repairs/sugden_a25/IMG_0426.jpeg" />

The Sugden measures around 110 mA on either channel. I tweak both trimmer pots to set the bias current to 90 mA. Then I wire the input and output of the Sugden to an oscilloscope and check how well the output matches the input when feeding a 5 kHz sine wave. The scope trace looks excellent — repair done!

When the customer comes to pick up their amplifier he tells me that the amplifier has been turned on for most of its life. This explains the rectifier capacitor issue perfectly. Thes rectifier capacitors have been derivering for 40 years, they've held up well: The new ones have something to live up to.
