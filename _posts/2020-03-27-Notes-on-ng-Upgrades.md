---
layout: posts
title: "Personal notes on Upgrades for the HCAL"
categories: HCAL Upgrades
author: Uzziel Perez
meta: "Next Gen stuff without much details"
math: true
---

I have been assigned to fix a certain issue. The idea is quite simple. LED light from the physical electronic parts turn on when we configure a run. That causes noise so it has been requested that we turn that off during a run. I talked to some seniors about the relevant files and how I could possibly approach the problem. Quite simple in principle but I need to figure out how the different files go together, and what variables control the LED for the different sections of the HCAL. Sort of... The solution is not very clear in my head yet.

Before I begin sifting through the codebase for relevant files, I just want to review the notes I made before the pandemic started.

### An intuitive explanation para mi

*These are notes and might not be very accurate. Am just writing for documentation and for my understanding. Unfortunate that personal blogs don't have a robust self-correcting mechanism yet. Also, need extra motivation to figure this out. Also, flexing a bit.*

I talked to our postdoc and he was pretty good at explaining things in a less technical way for someone like me who's just getting started. I'm just going to write in broad strokes how parts are connected.

 The next gen (ng) Clock and Control Module has a server which is some kind of brain that talks to the ng Front End electronics that then talks to the readout box. The software we have is what talks to the the server. We don't really have direct communication to the Front End electronics.

 The server fetches you the register values. For this I'd probably have to edit the ng Read Out box manager source file. Write the registers and commands and test. Still going to figure out this part.

 Monitoring stuff are long-lived applications. The "manager" stuff only runs when configuring.

 Just want to add  "Configured" means settings for the software are loaded and applied from database. "Running" means ready to receive triggers and readout events.

For bookmarking purposes, I like this concise [paper](https://www.sciencedirect.com/science/article/pii/S240560141500646X) on HCAL upgrades written by our postdoc. I should write a more public-friendly version of this next time. It will probably help me understand things more.
