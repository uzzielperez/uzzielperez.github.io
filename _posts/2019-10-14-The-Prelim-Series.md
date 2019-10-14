---
layout: posts
title: "The idea behind Luminosity in the LHC."
categories: Prelim Series
author: Uzziel Perez
meta: "Preparing for the prelim"
math: true
---

Collider physics papers normally report the amount of data they collected in terms of "Luminosity" $$\mathcal{L}$$. It wasn't very clear to me what it meant so my adviser "friendly grilled" me about it and we went down to the very basics.

One of the first things we think about when it comes to the actual data we collected is the number of events that we can get out proton-proton collisions.

\\[ N = \varepsilon \sigma \mathcal{L} \\]

We can move things around and solve for the Luminosity. We can assume that the efficiency $$\varepsilon$$ is just 1. But what is the cross-section $$\sigma$$ here and the number of events N?

Cross-section is measured in terms of area. If we assume that protons are spherical and has a radius of 1 fermi or $$1\times10^{-15}$$ meters then the contact area of two protons colliding would be approximately $$A = \pi r^2$$. If we plug in the numbers that would be $$A = \pi (1 \times 10^-30) \textrm{m}^2$$. Knowing that 1 barn (b) is equivalent to $$ 1 \times 10^{-28} $$ m^2 so the cross-section for individual proton-proton (pp) collisions is about 30 mb. We can assume that if the protons just slide past one another that the electromagnetic force between them are negligible since the "strong force" that binds the gluons, quarks and the "sea" of particles inside the protons is much stronger.

<img alt="Lumi" src="{{ "/assets/img/Lumi.jpg" width="20" height="20"| prepend: site.baseurl }}" />s

It's quite hard to align individual protons together. They're so tiny it's nearly impossible to align them to be on collision course. So in the LHC, proton beams are made. These proton beams are composed of bunches of protons. There are about $$10^{11}$$ protons in these bunches that collide every 25 nanoseconds (ns). Most of the protons here don't even meet. There are only about 20 collisions per bunch crossing. Knowing that there are about $$300 \times 10^5$$ s in a day, we can divide that number by 25 ns and we have around $$1 \times 10^{15}$$ bunch crossings per year. The LHC was on for about 3 years, so with 20 collisions per bunch crossing, there would be about about $$10^{16}$$ events from pp collisions. We can get this same order of magnitude in another way. The recorded integrated luminosity for Run II was $$139 fb^{-1}$$ so if we multiply that with the cross-section for individual proton-proton collisions that would be $$10^{16}$$ events! That's a lot of information to store! This [video](https://www.youtube.com/watch?v=jDC3-QSiLB4) shows how the LHC processes data. Of course not all of these are recorded. I'll probably write about event filtering later.
