---
layout: posts
title: "Calorimeters"
categories: Prelim Series
author: Uzziel Perez
meta: "This is where the particles leave their energy"
math: true
---

## Calorimeters

I'm about to wrap up my review for the prelim exam with a few more blog entries on particle physics. I'm going to follow up on the LHC blog with a more detailed discussion on calorimeters. Need to do this for my own understanding!

Calorimeters are materials that are used to absorb the energy of particles. The energy absorbed can then be measured depending on how the material reacts, e.g. it would change temperature or emit light when they get excited.

We talked about the electromagnetic calorimeter (ECAL) and hadronic calorimeter (HCAL) in a previous blog. The ECAL measures electron and photon energy. The amazing thing about the ECAL is it's made up of more than 70,000 beautiful lead tungstate crystals. These crystals are special as they both perform the task of an absorber and an active medium. As a photon or an electron encounters a nucleus in the crystal, the photon pair-produces while the electron undergoes "bremsstrahlung". "bremsstrahlung" is a German word that comes from "bremsen" meaning "to break" and "Strahlung" which means "radiation". So whenever an electron or a charged particle hits an atomic nucleus, it gets deflected and emits a photon. You can imagine that when the photon produces a pair of e+ e-, the e+ e- would "Brem" and then the photon coming out would pair produce again and this process continuous on like a tree branching out. This is called an electromagnetic shower and is shown below. I got the crystal image from cds and the electromagnetic shower from [here](https://www.mpp.mpg.de/~menke/elss/).

<img alt="Lumi" src="{{ "/assets/img/leadtungstate.jpg" width="10" height="20"| prepend: site.baseurl }}" />

<img alt="Lumi" src="{{ "/assets/img/shower.png" width="20" height="20"| prepend: site.baseurl }}" />

When the crystal has absorbed enough of the electron or photon's energy and it goes down to ev-range energies, this will excite the atoms in the crystal and then radiate light when it drops down to its original state. This process is called "scintillation".

Another jargon I need to understand is "radiation length". It's the "characteristic amount of matter traversed" by the shower. It's defined as the "mean distance over which a high-energy electron loses all but 1/e of its energy by bremsstrahlung" and "7/9 of the mean free path for pair production by a high-energy photon" (see [pdg p18](http://pdg.lbl.gov/2011/reviews/rpp2011-rev-passage-particles-matter.pdf)). To be honest, it's still not very clear in my head what it is. Need to discuss this and the Moliere radius with my adviser. The later is related to the transverse development of the shower. It scales with the Moliere radius.

The pretty lead tungstate crystals are super expensive. But they were worth it! I think the story is that CMS spent a lot of money on the ECAL because they were banking on finding the Higgs boson when it decays to two photons ($$H->\gamma\gamma$$). They did find it in 2012. So because of budget constraints, they could only build the HCAL with a "sampling" calorimeter with a poorer resolution. "Sampling" means it has alternating layers of "absorber" and fluorescent "scintillator" materials. I couldn't find a good picture but just imagine that the absorber is thicker and you sandwhich a thin scintillator layer in between the absorbers. As the particles pass through the HCAL you only "sample" the energy and don't have the ability to measure it everywhere.

The nice thing about calorimeters is that energy resolution improves with the energy of the particle. It goes as $$1/\sqrt{E}$$. So this is very good for high-energy physics (HEP) experiments.

I think that's all the studying I'll do for today because I'm tired.
