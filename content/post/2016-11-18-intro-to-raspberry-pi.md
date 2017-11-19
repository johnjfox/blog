---
title: Intro to Raspberry Pi
author: jjf
date: '2016-11-18'
slug: intro-to-raspberry-pi
categories:
  - tutorials
  - pi
tags: []
subtitle: ''
---

Over the last year or so, I've received several questions about where to start with a Raspberry Pi. Rather than repeating myself, I thought it might be easiest to just answer things once in a shareable format. I'll try to keep this README more or less up to date and will also place some sample code here if it will help anyone get started.

<!--more-->

## Some Caveats and General Statements:

- The Pi is a general purpose computer running a Unix operating system. depending on what you're hoping to do with it, occasionally you'll have to dive onto a command line and get your hands dirty. You'll also have to be comfortable with your "google-fu" of digging around on the internet for help. if either of these things don't sound like something you'd like to do, playing with a Pi might not be for you.
- Conversely, the Pi is a fun platform for creating various flavors of projects that make a computer interact with "the real world". I personally find it to be a lot of fun, but please keep in mind that I'm an electrical engineer by training and have a PhD in robotics, so this is kinda my sweet spot for intellectual fun. Your mileage may vary. Having said that, the Pi is a platform that was developed explicitly for teaching these types of things to relative young kids, so it's definitely doable if you are interested.
- To give you an idea of some the things I've been doing, some projects I've done over the last six months or so (with the add ins required to build them):
	- built a home streaming media server 
	- built a small maze game with a pan and tilt capability (required an add on board)
	- built a small drum kit synthesizer (didn't really build much here; it was a demo for a sensor board).
	- built a small weather monitoring station for my office (required an add on sensor board). Yes, I can already hear the gentlemen that typically sit in the back of our classroom saying that it's unlikely to rain in my office. That's probably true. I was mostly looking to see if I could host a NoSQL database + a web service on the pi to serve data and data histories up on demand across the internet
	- built a small mobile robot (required a robot chassis and a small add on board to drive the motors)
	- built an Alexa device (required a speaker and a USB microphone. I'm currently integrating Alexa into the robot as part of a larger objective of creating a talking zombie teddy ruxpin. Yeah..... long story
	- Anyway, you get the point. For the most part, these projects have been pretty simple as far as such things go since I'm pretty time constrained, but it gives you a sense for the types of things you can do.

## What web sites should I know about

Some sites to check out before you decide to invest:

- [Raspberry Pi Foundation](https://www.raspberrypi.org): The project section may give you ideas on things that you can do. Also, the weather station and the tilt game were built using the AstroPi board
- [Adafruit Raspberry Pi Shop](https://www.adafruit.com/category/105): Lady Ada is a leader in the maker movement and her online store is one of the best US based resources. I would recommend buying here since her prices are consistent with everyone else and she's definitely worthy of the support. There are tons of useful tutorials for beginners through more advanced users for all manner or "maker" related projects
- [Pimoroni](https://shop.pimoroni.com): A UK based developer of various external boards and cases. I have lots of there stuff (and will recommend some below). Worth taking a look at.

## What should I get?

### Minimal Setup (circa November 2016)

- A Raspberry Pi 3 (the current model)
- a 5 Volt (5V) power supply with a microUSB cable. Lady Ada has one that supplies 2.4 Amps (2.4 A) which is nice. There is also an "official" one. No matter what you get, you need to have at least 2.0 Amps (2 A), but I recommend a little bit more (i.e. the 2.4 A) because things can get squirrelly if you start attaching the Pi to other devices and you don't have enough amperage.
- An SD card
	- Specifically, you'll want a microSDHC card. You'll probably also want one that is bundled with a small adapter so that you can use it in your computer to create your operating system disk, do backups, etc.
	- I recommend at least an 16 GB card. if you're going to collect data onto the card, then obviously more space is better than less.
	- You can purchase one that is
		- (a) blank, in which case you'll need to either follow the installation instructions from raspberry.org or ask me for help and I'll make a copy of my setup onto your card. This is the cheapest option, but you're trading your time for money.
		- (b) has a copy of the current operating system already installed. The most current is from September 2016
		- (c) or has something called NOOBS installed which is a startup program that will guide you through the set up process. 
- (Optional) An HDMI TV to use as a monitor for the Pi. This is by far the easiest option for a newbie since it just plugs in. Alternatively, you can use a "headless" setup where you log in from your laptop, but this may be a challenge for some folks
- (Optional) An HDMI cable to hook it up to the monitor if you go this path
- (Optional) A USB mouse and keyboard to interact with the Pi. Again, this is by far the easiest option, although if you go headless then it's not required
- (Optional) A case of some flavor. I've been through quite a few options here and I prefer the Pimoroni and C4 Labs cases. My current favorite is the [**Pimoroni Pibow Coupe**](https://www.adafruit.com/products/1984) which is extremely solid and leaves access to the pins. It's a bit more expensive than many but I think it's worth it.

**ALTERNATIVE APPROACH** 

If you don't want to pick all of you own stuff, then you can buy a starter kit on both adafruit.com and Amazon. I'd personally stick with Lady Ada :). The main advantage here is that you get most of what you need to get things moving + the ingredients for some starter projects as well

- The [**adafruit Starter set**](https://www.adafruit.com/products/3058) has almost everything you need + a bunch of electrical components that you might enjoy using as a started into tying the Pi into the real world. **Note that this doesn't include the keyboard, mouse, or HDMI cable** You can purchase this with or without the Pi.
- Alternatively, the [**adafruit Computer Starter Kit**](https://www.adafruit.com/products/1806)  has the keyboard, mouse, cables, and SD cards but none of the additional components. You can purchase this with or without the Pi.
- The [**Microsoft Internet of Things Kit**](https://www.adafruit.com/products/2733) is a nice starting point for a lot of projects and comes with or without a Pi. The important thing to note here, though, is that despite it being the result of a partnership with Microsoft, I don't think you're locked into Windows.
- The [**official starter kit**](https://www.adafruit.com/products/3277) will give you everything you need other than a monitor. I think it's pretty expensive though 
- Amazon carries several kits that might result in a good deal e.g. ones from Canakit. I can't say, since I've bought virtually everything from adafruit. 
- Similarly, there is a company named [**Sparkfun**](https://www.sparkfun.com) that is similar to adafruit and has their own set of starter kits. make sure you get a kit for the Raspberry Pi 3, though.

### Interesting Add Ons

General advice: the Pi by itself is fun but the Pi with some other add ons to interact with the real world is an absolute blast if you're into such things. **HOWEVER: Be careful that whatever you buy is fully assembled. Many add-ons come in the form of "mini-kits" which is to say that they require you to solder together some pieces.** This may or may not be something you want to deal with. At the very least it will require you to have a soldering gun/iron + some minimal level of skill with soldering. With that said, here are some items I've had fun with

* [**The Pi Sense hat**](https://www.adafruit.com/products/2738): Multiple sensors + an 8x8 LED panel + mini-joystick. Only problem is that the temperature sensor will only measure the temperature of the Pi if you assemble it the normal way. Otherwise a lot of fun. 
* [**The Explorer Pro hat**](https://www.adafruit.com/products/2427) Lot's of ways to go here. You can attach motors, sensors, there are built in LED's, and touch pads
* [**Flotilla Starter Pack**](https://www.adafruit.com/products/3247) A ton of plug and play components. Very easy to use the hardware. However they're just graduating from a kickstarter campaign and the immaturity shows, especially on the software side which is quite immature. You can buy individual pieces directly from Pimoroni.

### Some Books

#### Introductory Books
* [**Adventures in Raspberry Pi**](https://amzn.com/1119046025) A lot of people like this book. Be careful though, because a new edition covering the Pi 3 is imminent. Most of the content is still relevant, but for someone completely new to this, it might be confusing. very step by step though, so if that sort of thing is what you're looking for then this might be ideal.
* [**Getting Started with the Raspberry Pi**]( https://amzn.com/B01I28HXIS) A pretty good introduction especially for complete newbies.  
* [**Programming the Raspberry Pi - Getting Started with Python**](https://amzn.com/1259587401) A lot of folks like this book. Note that it's also for the Pi 2.0, but most of the material will carry over. The big issue is that you have Wifi and Bluetooth built into the Pi 3.0.
* [**The Raspberry Pi Cookbook**](https://amzn.com/1491939109) A bit more advanced, but I personally like the cookbook style of books. 

#### Project Books
There are a ton, but here are a couple that are a bit more interesting than most

* [**Raspberry Pi for Secret Agents - Third Edition**](https://amzn.com/1786463547) The projects here are fun, but they go beyond the very basic and will require additional hardware to be purchased. 
* [**Raspberry Pi Projects for Evil Geniuses**](https://amzn.com/0071821589) and [**Raspberry Pi Electronics Projects for Evil Geniuses**](https://amzn.com/1259640582) A pair of books with "fun" projects. Yes, there is a trend here.
* [**The Maker's Guide to the Zombie Apocalypse: Defend Your Base with Simple Circuits, Arduino, and Raspberry Pi**](https://amzn.com/1593276672) More than Raspbery Pi, but, honestly, can you afford not to read this book?
