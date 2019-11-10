---
layout: posts
title: "Understanding Symmetry Breaking (Part II)"
categories: Prelim Series
author: Uzziel Perez
meta: "Explaining Symmetry breaking to my college self"
math: true
---

## Fourth of July

It was the fourth of July in 2012. I was a new college graduate and was working at a science museum when the Higgs Boson discovery was announced! From what I've heard later on from people working at CERN, both ATLAS and CMS have already found signs of a "Higgs-like" particle a year earlier. But these guys are very careful. A 5-sigma result is required before any discovery can be claimed in particle physics. For those more familiar with the p-value, $$5 \sigma$$ corresponds to a p-value equal to $$3 \times 10^{-7}$$. Pretty far from the 0.05 threshold!

Take a look at the evolution of the CMS data over time!

![Alt Text](https://twiki.cern.ch/twiki/pub/CMSPublic/Hig13002TWiki/HZZ4l_animated.gif)

## What does the Higgs do?

We talked about fermions (fundamental matter particles) and gauge bosons, the particles that guide their interactions and mediate the four fundamental fources (except the graviton hasn't been found yet!). What does the Higgs do?

So, if I was back with my Lyft Driver from Chicago, I'd talk to him about the beginning of the universe which he was very fascinated about. Right after the bigbang, most particles were massless and were zipping through space at the speed of light. It was very hot then. It began to be slightly cooler, and some form of symmetry breaking occured and here the Higgs field turned on and permeated the entire universe. The Higgs field is often likened to a thick syrup that slows down the particles, essentially by making them massive. This field gives mass to fundamental particles like the electrons, quarks, the W and Z bosons. Protons and other composite particles, particles that can be broken down into pieces, do not get their masses from the Higgs field.


## Spontaneous Symmetry Breaking

The W and Z bosons acquire mass through Higgs field through the process of "spontaneous symmetry breaking". I think every particle physicist should be able to explain this to a guy or girl in a bar. Three groups of physicists independently proposed this mechanism, but the process was only oddly named after Peter Higgs. The other guys were Englert and Brout, and Guralnik, Hagen and Kibble. I think it's because "Higgs" is super easy to pronounce and super catchy. But at some point it also got really famous as the "God" particle.

Here, I will be a little technical. Spontaneous symmetry breaking occurs through the introduction of a complex scalar field that gives rise the the SM Higgs boson. Fermions acquire mass through a Yukawa interaction of the Higgs boson.

A good visual example of a spontaneous symmetry breaking occurs in a ferromagnet. One can imagine the magnet to have little tiny arrows arranged in a grid. At first they are pointing in different directions and they have no preffered direction. So if you were living inside the magnet, you'd probably get lost. This occurs at high temperature. When you lower the temperature just enough, these arrows would then begin to align themselves. The magnetization then becomes zero because of this. Here, symmetry is broken.

Here is another visual image of symmetry being broken. If you rotate a rod about its axis, it doesn't look different. In that case, you call it "rotationally invariant". If there is a force that starts to bend the rod, you could then tell that it is being rotated.

I got the image from [this nice write-up](http://philsci-archive.pitt.edu/9295/1/Spontaneous_symmetry_breaking_in_the_Higgs_mechanism.pdf. The article also nicely explains the difference between "spontaneous" and "explicit" symmetry breaking. The latter occurs when there is an external force that actively breaks the symmetry. In math-y particle physics parlance you will find a symmetry breaking term in the Lagrangian, e.g. a mass term. In the case of the rod, that is called explicit symmetry breaking.

<img alt="Lumi" src="{{ "/assets/img/rod.png" width="20" height="20"| prepend: site.baseurl }}" />

To generate mass via "spontaneous symmetry breaking", instead of writing a mass term in a Lagrangian by hand, we can do something else. This is a typical example. Here I am simply regurgitating the discussion from Halzen and Martin Chapter 14. For a world composed only of scalars, we can write the Lagrangian as $$\mathcal{L} = \frac{1}{2} \left(\partial_{\mu} \phi\right)^2 - \left(\frac{1}{2} \mu^{2} \phi^2 + \frac{1}{4} \lambda \phi^4 \right)$$. Here $$\lambda > 0$$. The second set of terms in the parenthesis is the potential $$V(\phi)$$.

The idea here is that if $$\mu^2$$ is negative, the mass term sign is incorrect! And the potential would look like this.

<img alt="Lumi" src="{{ "/assets/img/potential.png" width="20" height="20"| prepend: site.baseurl }}" />

You can try to do some calculus for yourself and get $$\frac{\partial V}{\partial \phi} = 0$$ and solve for $$\phi$$ to get the extremum/extrema
You will find that when $$\mu^2$$ is negative, the extremum $$\phi = 0$$ where you were supposed to expect symmetry, does not correspond to the minimum. If we do some rewriting of the scalar field as a sum of the minimum and some quantum fluctuation about the minimum, $$\phi (x) = v + \eta(x)$$, the Lagrangian then will have a mass term with the right sign!

\\[ \mathcal{L} = \frac{1}{2}  \left(\partial_{\mu} \eta\right)^2 - \lambda v^2 \eta^2 - \lambda v \eta^3 - \frac{1}{4} \lambda \eta^4 + const. \\]

It's pretty late now. Around 1:30 am and still in my office. I should get back home and get some sleep. I'm also hungry. I'll talk about the Higgs mechanism after this.
