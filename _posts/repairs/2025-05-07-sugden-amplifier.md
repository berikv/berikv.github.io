---
layout: post
title: "Sugden A25 - Professional repair"
author: Berik
date: 2025-05-17 12:00:00 +0200
abstract: Capacitor replacement and new knobs for the Sugden A25
categories: Repairs
---

## Professional repair

A repairman asked me to repair his Sugden A25 amplifier. What an honour!

The machine works, but there is an audible 50Hz tone coming from the speakers. I immediately conclude that this must be the rectifier capacitors.

After recieving the machine and opening it up, there is a clear visual confirmation:
<img src="/assets/img/repairs/sugden_a25/06E4BA5D-E48B-404F-9BA7-ED197DA171A9_1_105_c.jpeg" />

Both capacitors have formed a slight buldge due to internal pressure buildup.

I remove both, and they measure 1000x less than their rated value. Due to the way they are laid out on the PCB, and the hight of the machine, I need to order the exact size: 35mm by 20mm, 10mm lead spacing. These are Rubicon branded capacitors, Sugden did select quality components! I can only order a batch of 500 Rubicon's of the correct value and size. I check in with the customer to see if they mind another brand. I get a reply of full convidence in my expertise and go ahead with the repair.

Lets be diligent, now I received full convidence. I inspect each component on the PCB and see some interesting features.

<img src="/assets/img/repairs/sugden_a25/DFCBE419-7B73-4E8A-8463-70F2D2EECCE7_1_105_c.jpeg" />
<img src="/assets/img/repairs/sugden_a25/A366D98F-8BA2-4872-94EC-5225AA1DD436_1_105_c.jpeg" />

Three things to notice here:

- The PCB seems to have been bent along the power transistor legs
- The PCB seems to has discolored around the transistors
- The ceramic capacitors have developed a white stupple beard

I first deal with the capacitors. Of each type of capacitor I desolder one or two, and measure their value out of circuit. There are quite some capacitors out of spec:
<img src="/assets/img/repairs/sugden_a25/C1294DC2-A971-48AF-8D16-717EAC0BC43A_1_105_c.jpeg" />

The two big ones are the rectifier capacitors that failed completely. The others still have some value, but less than specified (whatever it sais on the outside +/- 20%, for most capacitors). Also, ideally, if there are four capacitors with the same specified value, then you wouldn't want to see one being +20% and another being -20%.

I leave the capacitors that measure fine: They've survived over 40 years and chances are good they will survive another 40. For the out of spec capacitors on the foto I order replacements.

There is not much point in checking the amplifier without having good capacitors in place. Instead I can do some work on the front panel.
<img src="/assets/img/repairs/sugden_a25/AD626992-F186-4CEB-BAAA-A35DF43F41D6_1_102_o.jpeg" />

One of the knobs is missing, and another is split in two.

I ask a friend who has a 3D printer if they fancy printing a knob.
<img src="/assets/img/repairs/sugden_a25/A5924D2B-890C-4FAF-A1AF-22F52BDED6ED_1_105_c.jpeg" />

I measure and sketch the knob specifications, then visit my friend with this piece of paper. About an hour later we have the first attempt printed.
<img src="/assets/img/repairs/sugden_a25/052EBB59-468A-457B-A508-5311E9CB059F_1_102_o.jpeg" />

Here is the original knob on the left and the printed knob on the right. I ask my friend if the inset can be printed as well. Next they they deliver:
<img src="/assets/img/repairs/sugden_a25/C3B08F01-BC64-444D-BDFC-AAC035086574_1_105_c.jpeg" />

I spend 10 minutes per knob flattening the print patterns, then sand, then paint.
<img src="/assets/img/repairs/sugden_a25/DBDF2207-D0B3-42C6-AA77-FBDDCC127455_4_5005_c.jpeg" />

 One gets a different treatment. Being printed in red, I add a few layers of red spray paint with a nice gloss.
<img src="/assets/img/repairs/sugden_a25/728F99A1-C5CC-45A7-BE14-8B9144B23DE3_1_102_o.jpeg" />

I'm proud of the result:
<img src="/assets/img/repairs/sugden_a25/43D713BD-6054-41CF-A7AA-EC3AE0B78C6C_1_105_c.jpeg" />
<img src="/assets/img/repairs/sugden_a25/CDF1085A-D216-44C5-BBB9-BD44AAACD2CE_1_105_c.jpeg" />

I fix the knobs in place with some silicon glue. This type of glue does not become fully hard, so the buttons can be replaced later if needed.

I show the result to the customer: "A Red button?!" he responds jokingly. I tell him he will receive an extra black button and can decide which one to use himself.

Once the capacitors arrive by mail, I continue with the electrical repair. With the new capacitors in place, I test the amplifier. The volume button crackless when turned. Otherwise the amplifier works as expected. The 50Hz humm is gone.

I fix the volume button using some contact spray. Spray a bit of contact spray inside the potentiometer, on the Sugden that's the blue box right behind the volume knob. Then rotate the volume knob for a minute or two up and down.

Lastly I apply some silicon glue to all the capacitors. This amplifier won't be shaken much, still, I want to deliver quality. Some silicon glue relieves the stress that the capacitor leads bare when the amplifier is moved or shaken.

Time to go for the extra mile. I check the documentation for the bias current and find it should be somewhere between 80 and 100mA. To measure the bias current, remove one of the four fuses close to the power mosfets and replace it with a multimeter in current measure mode.

The Sugden measures around 110mA for either channel, I tweak both trimmer pots to set the bias current to 90mA. Then wire the input and output of the Sugden to a scope and check how well the output matches the input when feeding a 5kHz sine. The scope trace looks excellent, repair done!
