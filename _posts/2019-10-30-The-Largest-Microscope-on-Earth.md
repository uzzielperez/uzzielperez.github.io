---
layout: posts
title: "The Largest Microscope on Earth"
categories: Prelim Series
author: Uzziel Perez
meta: "Probing the smallest of things"
math: true
---

## Small Stuff requires Small Wavelengths

How do we probe the smallest of things? When we want to look at something closely, we can use a magnifying lens, typically a convex lens, and the parallel light rays from the object we're looking at would get bent and diverge at some distance behind the lens. The ratio between the image's height and the object height is the magnification. You can obtain the same number by dividing the image distance by the object distance. This means you can move the lens back and forth to adjust the magnification. For smaller objects, we can put together a set of lenses and make fine adjustments in the distances between the lenses and the object.

When using magnifying lenses and optical microscopes, we are typically looking at objects whose sizes are greater than or comparable to the wavelength of the light that we're using to look at them. So, what happens when we need to look at something smaller than a single-celled organism, maybe something smaller than an atom? We'd have to really go down to ultra-short wavelengths that are no longer visible to the human eye!

In order to go to ultra-short wavelengths, we have to review Heisenberg's uncertainty principle. I found [this](https://theory.uwinnipeg.ca/physics/quant/node7.html) to be a good additional reference but I'll also explain it here. For us to "see" small things, we need to shine "light" of a certain wavelength $$\lambda ~ \Delta x$$. (I put quotation marks on light because we could use other small particles like an electron too.) Light also has a particle nature and therefore has a momentum $$p$$ when it hits the particles we are probing. The uncertainty principle asserts that it's impossible to know simultaneously the exact position (wavelength) and momentum of a particle. So, the more precisely we measure the position, or the smaller the wavelength, the higher the momentum or energy of the light! If we need to look at really small stuff, we need high energies! You can try to calculate the needed energy yourself by using $$\Delta x \Delta p \geq h/4\pi$$.

So what we do in my line of work is to smash protons travelling close to the speed of light. After protons are accelerated to 99.9999% the speed of light, they travel in circular beams that are made to collide. How small are the things we are looking at? We're looking at things in the order of a femtometer or $$10^{-15}$$ m. For comparison, the width of a human hair is about 20 micrometers or about $$10^{-7}$$ m. It's more than a million times smaller! We're all doing this at the Large Hadron Collider (LHC).



## The path of a proton in the LHC

Everything starts inside a bottle of hydrogen gas that's about a little bigger than the water bottle I carry with me for work. It's incredible that for the entire lifetime of the LHC, we'll never have to refill that bottle again. There's about $$6\times 10^{23}$$ hydrogen atoms per gram of $$H_2$$ gas. There's definitely more than 1 gram there. So many protons! And electrons. But we only need protons so how do we get rid of the electrons?

Hydrogen atoms consist of a single positively charged proton and a single electron that are bound together. You need a high enough electric field that would pull the proton in the direction of the field, and the electron going the other way. This process is called ionization. Once you get the protons, you then bring them through a pipe that has segments with electric fields that alternated in direction with time. Each time the proton goes through a gap, the voltage reverses so that it can feel an electric force in the right direction. The machine that does this is called a Linear Accelerator or Linac. In the LHC, this is only the first in a series of accelerators. The Linac serves as an injector to a circular Proton Synchrotron Booster or just "Booster". When the protons come out of the Linac it already has an energy of 50 MeV. That's about 250 times the energy of a medical x-ray photon.

![Alt Text](https://media.giphy.com/media/EEwz0x1p1vTDXgG5yP/giphy.gif)

When the protons come into the booster they come in controlled "bunches". They get split into four and a section of the booster has a varying electric field that can be likened to a child being pushed in a swing each time they get back to their starting position. In this way, they get boosted and become faster. They come out about with about 30 times the energy with 1.4 GeV. I honestly had a hard time imagining how the booster works. This [video](https://www.youtube.com/watch?v=b6CqmHREE1I) probably has the best animation and explanation. I'll leave the rest of explanation on the accelerator complex to the video above and an excerpt from my dissertation proposal below.

> **The beam is then injected to the circular Proton Synchotron and then to the Super Proton Sychrotron (SPS) which accelerates the beam to 25 GeV and 450 GeV respectively. Finally, it reaches the LHC where RF (radiofrequency) cavities are used to accelerate the beams to the final center-of-mass energy of up to 14 TeV. There are two counter-rotating beams entering the LHC and they are brought together at four interaction points (IPs) where detectors are placed. These IPs are at the 4 major experiments at CERN that includes CMS."**


I recommend this official CERN video on the [path of the protons](https://www.youtube.com/watch?v=pQhbhpU9Wrg) and this cute [cartoon](https://www.youtube.com/watch?v=BEnaEMMAO_s) from Oxford.


## Giant "Cameras" and Tinder for particles

Once the two counterrotating beams meet at one of the interaction points, let's say within the CMS detector, you get a spray of debris. There'd be about 20 collisions per bunch crossing. Each bunch is spaced 25 ns apart. That's a lot of data to analyze. In fact, the data produced at the LHC and the individual experiments are comparable to the amount of data corresponding to all Facebook uploads per year. And [this information](https://slideplayer.com/slide/9416127/) was from a 2014 report from the CERN IT department!

When the debris come out of the collisions? How do we know which particles are which? How do we store information?

The CMS detector is built like a cylindrical onion which has one layer of subdetector on top of another. You can find an interactive cutout here. To put it simply, we particle physicists play a game of "connecting the dots". We piece together the information left behind by the particles in each of the subdetectors.

We know that particles like photons and electrons leave most of its energy in the electromagnetic calorimeter (ECAL). While hadrons leave most of their energy in the Hadron Calorimeter (HCAL). Muons don't really interact with the materials that much so they end up flying through everything and only leave traces of their presence in the muon gas chambers found at the edge of the CMS detector.

CMS, stands for "Compact Muon Solenoid". There's absolutely nothing compact about it. I think they only called it compact because it's a lot smaller than its "bitter rival", the ATLAS experiment. (lol. bitter rival is just a joke. They're two independent experiments meant to check each other.) The solenoid produces a magnetic field of 3.8 T and it is pointing in the direction along the beam pipe where the protons are coming in. This magnetic field bends charged particles and that gives information on their momenta. Charged particles also leave traces in the silicon tracker found before the ECAL. The information in the tracker allows us to further differentiate different particles. For example, if we see energy deposits in the ECAL (very little in the HCAL), how do we know if it comes from an electron or a photon? If there is a track in the tracker, it's most likely an electron since it's a charged particle!

![Alt Text](https://media.giphy.com/media/fLMqcN3gYXkas/giphy.gif)

We already know that we are dealing with BIG DATA from the LHC. There are about 600 million collisions every second and that corresponds to a petabyte of data per second. So in like 2-3 minutes, we can generate about the same data that all Facebook users upload in a year (in 2014). So, like in Tinder, we set filters! We choose only the most interesting events and "swipe left" to the uninteresting ones. And we lose that information forever. Lesson here: Set your filters right! You have to let in "interesting ones" and really "good ones". If your filter or selection criteria is too "tight" then you might throw in really good ones. You can "loosen" your criteria but at the expense of letting in a lot of "bad ones". There's a trade off! Now, I think the filters change depending on what scientists are interested in. In the end, we select only about 0.0000001% of all the possible data. Seems like real Tinder! (I haven't used Tinder though.) :P
