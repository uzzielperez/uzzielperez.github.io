---
layout: posts
title: "Big Picture Phase I"
categories: Physics, Dissertationn
author: Uzziel Perez
meta: "Do not drown in a sea of code"
math: true
---

*Do not drown in a sea of equations.* -Doc J.

Dr. Jerrold Garcia, or Doc J, was one of the most influential physics  professors in my college days. He was quite a strange guy. He was obviously looney and that made people gravitate towards him. And I would say he was the smartest physics prof ever in ADMU.

When I told my mom I wanted to do physics instead of taking a well-known "Management Engineering" course, we toured the different labs in Ateneo. While at the vacuum lab, there was this guy with a funny hair that came in. It was Doc J. The professor who was touring us told him, "she wants to move to physics." Doc J looked at me, and then my mom. Took a deep breath and his eyebrows furrowed. I thought he was going to say I wasn't welcome or something. After an incredibly long pregnant pause that seemed like an eternity he said "Nasisiraan ka na ba ng bait???!!!" ("Have you lost your mind?"). And then he smiled. I forgot what happened next but you know, the rest was history.

In his classes he told us not to "*drown in a see of equations*". To not forget about the "physics". That would guide the equations. And he also said that not everything in nature can be written in equations or formulas. And the closest thing we could do was code or do a numerical analysis or simulation of a certain model. Much of what I do now seem more of the latter. I let the phenomenologists or theorists do the equations and I run their models and compare with data.

I am writing this while am running code on 140000+ events which is a small subset of the simulation I am looking at. I just wanted to take advantage of the waiting time. I also sort of want to "celebrate" the culmination of a week's worth of debugging and restructuring of my code to comb through data. I like writing. It clears my mind.

Phase I of my work is about measuring the "photon efficiency". I might have mentioned in earlier blog posts that not every collision product is interesting or worth storing in memory. So we have what we call a "Trigger" which I call "Tinder for particles". If the event passes the "Trigger", they get stored in memory and we can "get to know them better"! In our parlance, we call this "offline analysis".

When we do our "offline analysis" we need to filter them further for quality. Sometimes, the photons we want are actually "fakes". For example, electrons and jets could interact with the detector such that they look like photons. But there are subtle clues that could let us tell them apart. Of course this is not a hundred percent fool proof. So there are several "strictness levels" in our filters or what we call "selection criteria.". For comparison, when you are super selective about people and you don't give others a chance, you can miss out on "real good ones". But then again if you're too "loose", you let in a lot of garbage too. You just have to be aware of the trade offs.

Since I am just really in the beginning phases of my Dissertation, the learning curve for me is quite steep. I am taking a while to make sure that the machinery works for my specific problem. And for a while, I forgot why we were measuring the efficiency in the first place.

Again, the goal of my research is to measure the cross-section of a rare physics process. From our data we could look at the number of events which is related to the cross-section [fb] and the luminosity [fb-1]. If we had a perfect 100\% efficiency then we'll get no "loss" in the number of events and we'd have a better measurement. An easy way to remember this is through this equation. The units of the cross-section and luminosity just cancel out.

\\[ N = \varepsilon \sigma \mathcal{L} \\]

So, this is where the importance of efficiency is. We have to make sure we aren't throwing away too many "photons" while suppressing the "fakes".

In the next phase of my research my goal is to determine the rate by which these "fakes" occur. This is important so that we could "subtract" the fake contribution from the data.

I'm a long way from finishing this work and I am feeling a mixture of excitement and nervousness. There are parts of the analysis that I completely know nothing about and I have to start the machinery from scratch. I will talk about them as I progress in my work.

Currently, my Ntuplizer is found [here](https://github.com/uzzielperez/multiphoton-analysis) and specific analysis code and some results are in a private repo (for quality testing purposes too!). I shall publicize them when I have finished my work so people can reproduce my work.
