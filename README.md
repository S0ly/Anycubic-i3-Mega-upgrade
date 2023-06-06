# Upgrading Guide for Anycubic i3 Mega

## Introduction

This guide presents a month-long project aimed at enhancing the performance of the Anycubic i3 Mega printer.

## Upgrade List and Costs

Here are the implemented upgrades and their respective costs:

- **Bed Isolation:** Improved bed isolation for better temperature control (€1.5).
- **Screws and Hardware:** Replaced various screws and components (€10).
- **Blower Fans:** Upgraded to more efficient blower fans for superior cooling (€10).
- **Motor Cooler:** Installed a motor cooler to avert overheating (€6).
- **Motherboard and Driver:** Upgraded the motherboard to SKR 1.4 and its driver to TMC 2208 (€45).
- **BLTouch:** Integrated a BLTouch sensor for automatic bed leveling (€42).
- **Extruder:** Enhanced the extruder mechanism  to a BMG(€20).
- **Hotend:** Upgraded the hotend assembly for improved printing performance to a dragon hotend(€80).
- **Cables:** Replaced cables for enhanced connectivity and reliability (€15).
- **Lubricant:** Applied superlube for smooth movement (€10).
- **PTFE Tube:** Replaced the PTFE tube for better filament feeding to a capricorne (€10).
- **Raspberry Pi 3:** Incorporated a Raspberry Pi 3 for advanced features (€40).
- **Night Vision Camera:** Installed a night vision camera for monitoring (€15).
- **Additional Fans:** Added extra fans for enhanced cooling (€30).
- **Cable Management:** Employed cable chains for cleaner cable organization (€10).

aproximate total of 350€

Additionally, the following components were 3D printed:

- **Bed Screws:** Four bed screws for improved stability.
- **Bed Grip:** Custom bed grip for enhanced adhesion.
- **X Carriage Mk-4:** Upgraded X carriage for better stability.
- **Raspberry Pi Case:** Case for the Raspberry Pi.
- **Night Vision Camera Case:** Case for the night vision camera.

## Printer Anatomy

The printer is divided into four main parts:

- **Upper Part:** Houses the print head, including the nozzle, a custom PCB for the printer, and the extruder motor.
- **Lower Part:** Contains the bed and all the electronic components, including the PSU, motherboard, drivers, and the hub (custom Anycubic PCB that facilitates communication between internal and external components, minimizing cable clutter).
- **bed:** is used to print on it its used as the Y axis
- **print head:** its on the X axis and the bar of the X axis are on the Z axis, its used to have the hotend in it a print the filament

## Disclaimer

Take heed of the potential hazards, especially when dealing with the PSU and other electrical components. Always prioritize safety; I am not liable for any accidents, damages, or injuries that may occur during the upgrade process.remember too that if you modify the cables and software your printer can damage itself by not stoping the motor or doing other strange thingsso I really recommend you to be really careful whit what you do

This is not really a detailed guide but more a text that explain what I have done to upgrade my anycubic i3 mega, I think this guide can work too for other printer. I have linked some resource and proved that certain things are possible and if you want you can achieve the same result. Good luck with your upgrades!

---

## Bed Upgrade

**How I Did It:** I started by disassembling the printer. I drilled holes in the bed structure and lower part to attach the chain and its mount securely. Then, I added the bed isolation materials to the bed surface. I had to adjust the Y-axis height since the chain was blocking the bed screws. This involved raising the bed by placing the Y-rod maintainer parts on the surface rather than attaching them below. I also adjusted the belt system and Y end stop to match the new bed height, I then added the bed levelling screw and handle

**Pros:**
- Better heat management
- Ease of movement
- Precision when adjusting
- Beautiful and practical cable chain

**Cons:**
- Loss of approximately 5mm of Z-axis

---

## Print Head Upgrade

**How I Did It:** I mainly followed the instructions for the X-Carriage Mk-4 designed for the Anycubic i3 Mega. I had to modify the X-carriage slightly to fit the Dragon hotend and install the blower fans. I used a custom PCB for managing cables and included a BLTouch sensor. Most cables needed to be replaced or soldered to new ones for a proper connection.

**Pros:**
- Clean cable management
- Easier maintenance
- Lighter print head
- Better cooling
- Includes a BLTouch sensor

**Cons:**
- Occasional need for minor modifications

---

## Upper Upgrade

**How I Did It:** I purchased and installed a BMG extruder, added a Capricorn PTFE, and included a motor cooler.
To do this upgrade you dont need any special thing just follow the instruction of the BMG extruder, for the PTFE just replace your actual one and for the motor cooler just put them in place like they are intended to be monted (you can place them on the back of the motor its fine the hole does not serve any purpose).

**Pros:**
- More consistent extrusion
- Better motor cooling

**Cons:**
- None found yet

---

## Hardware Upgrade

**How I Did It:** I printed a case for the raspberry pi and mounted it on the printer's side. After installing Mainsail OS on the pi and compiling Klipper for my printer, I replaced the old motherboard with the SKR 1.4 and flashed Klipper onto it using an SD card. After connecting everything, I installed the drivers. I replaced the hub PCB with a custom one and added a night vision webcam for monitoring the printer. Then you will need to configure everything and have the printer configuration file that you will tweak.

**Pros:**
- A multitude of new functions
- Quieter motor
- Enhanced security
- In-depth statistics
- Web interface
- Camera monitoring

**Cons:**
- Costly
- Requires considerable time and tinkering

---

At the end, if you follow all the upgrades like me, your Anycubic will be:

- **Much quieter:** With the upgrades implemented, your printer will operate with reduced noise levels.
- **Able to print more materials:** Thanks to the new PTFE and extruder, you will have the capability to print a wider range of materials.
- **Much faster:** The upgrades will enhance the printing speed of your Anycubic.
- **Better print quality:** You can expect improved print quality after implementing these upgrades.
- **Enhanced security functionality:** The upgraded printer will offer features such as detecting if everything is working correctly, emergency shutdown, camera monitoring, and more.
- **Additional fun functionality:** Enjoy features like more data and the live code viewer, adding to the overall experience.
- **Increased tools functionality:** Benefit from assisted bed leveling, bed leveling compensation, web interface, and more.
- **And much more!** Explore other exciting enhancements that these upgrades bring to your printer.

Of course, throughout this process, you will gain valuable knowledge and skills that will enable you to continue tweaking and fixing your printer if needed.

Thank you to everyone for the feedback, suggestions, and support during this journey. Your contributions have been invaluable in improving the Anycubic experience. Happy printing!

little bonus : I have here logbook that I have written while making the upgrade you can read it to see the problem that I have encountered in the process, it can maybe save you some on your side ! and i putted some hard to find / important documentation that could help you in the help-asset folder, dont thanks me :)

---

## Ai3M Modification Adventure Journal

### Day 1: Ignorance is Bliss

Checked the steps thoroughly, started to disassemble and inspect the printer, and captured the "before" photographs of the hot mess that is my 3D printer. In a stroke of sheer genius, prepared a DIY white background.

I also measured the noise level with the Apple Watch. It turns out that the printer sits comfortably between 70 and 80 dB (mind you, Apple Watch has a margin of error of 3dB).

So here's the current state of affairs:
- The printer is hotter than a chili pepper in a desert.
- It's stuck at a snail's pace of 40mm/s.
- It's dumb as a box of rocks, missing heaps of functionality.
- And it's LOUD at 80dB! Honestly, I'm not sure how I sleep with this cacophony in the background.

### Day 2 - Day 3: The Inception of Problems

I'll give you an overview of what I'm doing, but let's not bore you with the nitty-gritty of my research; that's a whole other can of worms best left for a guidebook.

In short, I desperately tried to implement the bed upgrade. I grossly underestimated this task, thinking it'd be a piece of cake. Oh boy, I couldn't be more wrong! An avalanche of unexpected issues descended upon me.

For instance, I totally overlooked the need for drilling holes. You might think, "Ah, just some holes, no biggie!" Wrong. We're talking metal drilling, folks! That means metal dust everywhere. And you know what's next to this dust? A 230V PSU. So there I was, disassembling and reassembling the electronics, keen on not blowing up my house! Of course, I cleaned the printer between these steps.

When I finally installed the cable, lo and behold, the wheels wouldn't pass because they were blocked by the cable. Long story short, I had to rearrange the Y-axis towards the Z-axis, and that's just the start of my woes.

It's all uphill from here, folks, and not in a good way.

### Day 4 - Day 5: The Nozzle and The Phases of Denis

I'd been eagerly waiting for this part—mounting the nozzle. It feels somewhat like playing with Lego, except I made these myself.

Right off the bat, I hit a snag. This carriage was designed for an E3D v6. I have a Dragon nozzle, which in theory, should be compatible with E3D v6 in terms of size and all. Well, guess what? Apparently, engineers paid thousands can't create a similar nozzle. So, I ended up having to modify the model—time-consuming and irritating, but hey, it worked.

It's funny how this part was here, serving no apparent purpose and causing problems for nozzles even slightly different from E3D v6.

And let's not forget the moment when my hawk-eyed self noticed something was off. After hours of tinkering, I found the issue: the 3D model was poorly made, despite its fame. Nothing a piece of plastic can't fix, right?

Well, after this fiasco, the nozzle was installed, the BLtouch was aligned, but wait—where's the BLtouch cable?

Then it hit me. The baseboard had 15 PINS! Only 8 out of 15 were being used, but it had duplicate connections. So, I HAD to add cables for the BLtouch which needs 5 by default.

Hours of soldering (

with my pathetic soldering iron), some board damage, and a less-than-optimal result later, I found a lovely person on eBay selling modified any cubic hotend PCBs that use all 15 pins. Now I could even add little LEDs—cool, right?

So after connecting everything and managing the cables, the nozzle was operational. Of course, let's not forget the time spent reassembling, greasing, and making a mess!

### Quick Bonus:
The old nozzle weighed around 310g. The new one, with more features, is only about 250g. How about that for an upgrade!

### Day 6 - Day 7: The Descent into Hell

Nothing went according to plan.

Upon inspection, it quickly dawned on me that NOTHING was going right:
1. There's NO documentation on the internet. Nada. Zilch. Zip.
2. The wiring between the default MB and the SKR 1.4 is vastly different.
3. Any cubic had the brilliant idea of customized cards and wiring, which makes the transformation to the SKR 1.4 even more complicated with their crappy bus.

Next, the SKR 1.4 couldn't latch onto anything, considering its different size and configuration. The cables were either wrong or too short, and the default labels from any cubic were incorrect. A label E01 meaning Extruder 1 makes zero sense, yet here it was, pointing towards the stepper motor 2 of the Y-axis. I was utterly unprepared for this level of chaos, and it was pure hell.

Each time I had to close the printer after inserting 8 screws, some cables would disconnect themselves. So, I had to turn it back, disassemble everything to identify the problem, reconnect everything and screw it back. Rinse and repeat, and no, not just ten times; I'm being generous here.

In the end, I managed to make everything work with a combination of luck, patience, and some trusty old scotch tape. I plan to order some more cables and redo this mess.

### Day 8:

The day was mostly spent attempting to make the motors and the end switches work correctly with the BLtouch. However, I still had to deal with the terrible configuration, and I'm considering redoing it.

This stage is the most terrifying as if something isn't configured right, the printer might just commit harakiri, and we don't want that.

Perhaps closed-loop drivers could solve this issue, but they are PRICEY!

Klipper, luckily, has a superb doc and plenty of cool tools to check if everything is functioning well. Although my config turned out to be utterly wrong (probably because I didn't read the Klipper doc properly, or the person who had this doc before either didn't read the doc or had different motors), everything went smoothly. Tomorrow, I'll likely redo the document.

Pro tip: Do not leave your phone in the printer's path because it will chew it up without a second thought. Same goes for your fingers, by the way.

### Day 9: Configuration Hell

As promised, I remade the entire configuration and continued educating myself on Klipper. I also tried to fix an issue with my raspberry that kept disconnecting from the wifi for no reason—yes, it took more time than it seemed. On the brighter side, I learned a lot about how the configuration works.

### Day 10

I tackled the next step today: the heating resistors, a bit of wiring, and the PTFE tube.

First off, I tried to play around with the fan for nearly 2 hours because I wanted it to switch directly from 3 to 2 pins without an extension. It quickly turned into a hellish ordeal that would have required soldering, so I reinstalled the adapter and continued.

Next, I tackled the PTFE tube, which was fairly simple. Cut, connect, and voila!

Then came the resistors so I could finally confirm that the extruder, the hotend, and the bed were functioning as expected. Testing the head and bed went smoothly until I heard a strange clicking sound.

After about six hours of investigation, I learned that this sound

 was, in fact, normal. Though it sounds like I figured this out in two seconds, it took a ridiculously long time and even made me a German friend on the way. While trying to fix what I thought was an issue, I'd actually exacerbated the problem: the PID tuning.

The clicking came from the PSU when it had to power the resistors. A couple of reasons why I only noticed the clicking now could be:

1. The new board is more precise and frequently asks the PSU to switch the temperature.
2. Since the printer only produces 40dB, I can hear the faint click more easily.

So, maybe I'll need a new PSU if I want to eliminate this annoying click.

In the meantime, I've added a great parameter to manually calibrate my printer. It now has over 1000 lines—crazy, right?

I ended the day by trying to print my first benchy, but an under extrusion issue due to incorrect stepper rotation parameters resulted in a terrible print. I also had to prepare the slicer for Klipper and still haven't solved the under extrusion problem. I'll have to deal with that tomorrow.

On a side note, when I say "day," it can be MUCH MORE than 7 hours of work. In this case, it was a whopping 18 hours.

### Day 11 - 12: Calibration Confusion

I assumed it would be plain sailing from here. Spoiler alert: It was not.

The reality hit hard. My configuration file was plagued with issues. I dived deep into the internet, scouring through every 3D printing forum and manual available. The culprits? Misaligned offsets, ill-calibrated extruder, a less than immaculate bed, and the BLtouch's functionality, which was shrouded in mystery.

Ah, the BLtouch! I thought it would be my knight in shining armor, rescuing me from the drudgery of bed leveling. Yes, it has the power to mitigate bed issues, but it's not the all-sufficient oracle I'd envisioned. It can compensate for unintentional bed deformities but not fix a poorly leveled bed. It's more of a sidekick aiding with manual leveling, rather than a solo superhero. The takeaway: nail the manual leveling as precisely as possible, and the BLtouch will assist from there.

Apart from that, I made some improvements here and there. And voila! I managed to print a rather satisfactory benchy at 100mm/s, with a tolerable noise level of 50dB.

### Day 13 - 19: Pushing the Limits

Admittedly, I've been a bit lax with my journal updates during this period. The highlight reel? I put my printer through the wringer, testing substantial prints, and pushing it to its limits. From exploring top speed to maintaining discretion, I ventured into it all, inviting a barrage of problems.

It took me two whole days to diagnose why the motherboard fuses were randomly blowing up—turns out, it was due to a misunderstanding of the wiring. Then, my BLtouch had a mid-print existential crisis, self-diagnosing, deploying, and crashing against the pieces, which took another two days to fix. The culprit? Bad connections necessitating a complete hub wiring overhaul.

Oh, and the extruder had jamming issues. After a lengthy investigation, the culprit was found—Noctua fan, not providing enough airflow, leading to heat creep.

I tried to make the printer better overall by tweaking the extruder system, meddling with the settings, and whatnot. I changed how the bed connected with the motor and the pulley system, rewired the internal setup multiple times, soldered countless cables. And while I jot down this journal entry, the printer testing continues relentlessly.

In conclusion, this venture required far more time and energy than anticipated, filled with countless surprises. But on the bright side, I achieved my goals! I've overhauled nearly the entire printer—the only original parts left being the motors, the PSU, the chassis, the bed, and two end switches.

In retrospect, building a Voron from scratch might've been easier. But hey, I now have a printer that can reach print speeds of 150mm/s (though I mostly stick to 100mm/s), producing noise levels between 40 and 50 dB. Not only that, it comes packed with a slew of new features, offering significantly improved print quality than before.

No pain, no gain, right?
