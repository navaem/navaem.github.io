---
layout: post
title: "Connecting a Fitbit to a Raspberry Pi 4"
description: "Often we don't think of a Raspberry Pi as an Android device. Turns out it can run Android and more"
comments: true
keywords: "bluetooth, raspberrypi, android, setup, lineage, OS, raspberry, pi, 4, versa, lite, fitbit"
---

**If you doubted whether connecting a Fitbit to a Raspberry Pi 4 is possible, let
me assure you it is and that I've done it.**

I bought a Raspberry Pi 4 in January and have been trying to sink my teeth into a good
project where I can use it. At the same time, I had been doing quite a bit of Android
development on this project that used Fitbit Versa Lites to measure health data. I don't
 own an Android device, and I didn't want to buy one just for this project. This situation
 led me to think, 
*If Raspberry Pis run Linux and Android is a Linux flavor, surely I can boot Android
on my Raspberry Pi.*

## How does a Fitbit Versa Lite connect to a phone?

The Fitbit Versa Lite is the cheapest smartwatch offering in the Fitbit lineup. Being the 
least expensive, Fitbit has cut cost on this model by leaving out some desired features
like wifi and GPS, but the Versa Lite still has a leg up on the even cheaper tracker lineup 
because of its LCD screen. Lacking wifi capability means the Versa Lite must always 
be tethered via Bluetooth to a phone with the Fitbit app installed. Unfortunately, Fitbit 
requires all communication with their devices to go through their app in one way or another.

## How to run Android on Raspberry Pi:

I found a great port of an existing open-source Android version,
[LineageOS](https://lineageos.org/), to Raspberry Pi done by KonstaKang
[here](https://konstakang.com/devices/rpi4/LineageOS17.1/). 
Using this port greatly simplified the task at hand as KonstaKang has already
taken care of the heavy lifting for us, for example integrating the OS and the firmware 
and drivers. Once we flash the port onto our microSD (install instructions:
[Linux](https://www.raspberrypi.org/documentation/installation/installing-images/linux.md),
[Mac](https://www.raspberrypi.org/documentation/installation/installing-images/mac.md),
[Windows](https://www.raspberrypi.org/documentation/installation/installing-images/windows.md)) 
that the Raspberry Pi uses to boot, we can start up our Raspberry Pi running Lineage OS. 

Unfortunately, Lineage OS comes without gapps and the Google Play Store, meaning we
won't be able to install the Fitbit App. 

## How to setup and install Google Play Store Konstakang Lineage 17.1. 
Watch this video and follow its instructions to install the Google Play Store on your Raspberry Pi 4.
<div class="video-container">
    <iframe  src="https://www.youtube.com/embed/3i2h9JgPPME" frameborder="0" allowfullscreen>
    </iframe>
</div>
Video Link: [https://www.youtube.com/watch?v=3i2h9JgPPME&feature=emb_title](https://www.youtube.com/watch?v=3i2h9JgPPME&feature=emb_title)


Once your device reboots, you can install the Fitbit app using the Google Play Store and sync 
your Fitbit with your Raspberry Pi just like you would any Android. If you need help, you can
always visit the [Fitbit help docs](https://help.fitbit.com/articles/en_US/Help_article/1873.htm).
Your Raspberry Pi's Bluetooth chip must be functional because the Fitbit Versa
Lite can only communicate via Bluetooth.

## Congratulations!

At this point, you should be able to connect your Fitbit to your Raspberry Pi, and you can begin
thinking of Fitbit development ideas. Fitbit has a pretty good 
[development SDK](https://dev.fitbit.com/) and developer docs. Doing a 
[quick search on Github](https://github.com/search?q=topic%3Afitbit-devrel+org%3AFitbit&type=Repositories),
you'll find lots of open source projects that you can take inspiration from or fork. 

Happy coding!

