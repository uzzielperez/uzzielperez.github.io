---
layout: posts
title: "HCAL Part I"
categories: General
author: Uzziel Perez
meta: "Getting to know the CMS Hadronic Calorimeter"
math: true
---

I'll be working on the HCAL subdetector software for the forseeable future. I feel like I don't know enough about it so I'm going through the technical report, [TRD](https://iopscience.iop.org/article/10.1088/1748-0221/3/08/S08004/pdf) and the papers on the Phase I upgrades like [this](https://reader.elsevier.com/reader/sd/pii/S240560141500646X?token=88069C18EB0AC54A00A09E6EEF6FE827D5DB1F392F21AA39ED2B174F98E1C1C6BB818789AA2D578CE0D10B97D91FA6BE). A lot of their contents went through my head the first time so I need to read them multiple times and connect them with the software code I am testing.

So my goal here is to describe what the HCAL does, have an overall picture of how data is collected and have a better understanding of how the software communicates with the detector. (And also to understand the many acronyms like HTR and QIE).

# What's a calorimeter?

A calorimeter is something that measures a change in energy. 'Calor' is a word associated with 'heat' and 'meter' is associated with measurement. A simple calorimeter can be made at home. You just need a material that has an attribute that could change with the amount of the heat absorbed. For instance, water in a styro coffee cup. To measure the heat it absorbs from a burner, we can measure the change in temperature. The heat absorbed is just equal to the temperature multiplied by some factor, usually the mass or the specific heat of the liquid. To have more "reliable" results, we need to make sure that there's no unwanted heat transfer to the environment. Also, moar data, moar trials the better.

In particle physics, typically, calorimeters measure the energy of particles like photons, electrons. It could also measure a spray of particles. Each of them have their own "signatures" in the different subdetectors. I think I talked about this some more in [here](https://uzzielperez.github.io/prelim/series/2019/10/30/The-Largest-Microscope-on-Earth.html).

When the particles hit the calorimeters, they will interact with the material. In the *electromagnetic calorimeter* (ECAL), the photons and electrons will hit the crystal nuclei and that would start an electromagnetic *shower*, where e+e- pairs are produced and lower energy photons are radiated in a tree-like fashion. The sum of all the particles in the shower then tells us about the energy of the incoming particle. These particles at some energy scale would then excite the atoms in the crystal, and they will scintillate or produce light that can be collected and "read electronically". (I'm jumping a bit. I will discuss about signal transformation and electronics later).

For the CMS HCAL, it's a bit different. The calorimeter is not homogenoeus (it absorbs energy AND scintillates). Instead, HCAL is made up of alternating materials. A very dense material to absorb the energy, i.e. to cause a shower and a thin layer of scintillating material. It's a brass/scintillator *sampling* calorimeter. Since it's only sampling, sometimes not all of the energy is measured accurately, i.e. the shower is not deposited in the right material, and therefore is not included in the measurement. We say then that, the homogeneous calorimeter, ECAL has a better than the HCAL. If they were compared to phone cameras, you could say, ECAL is an iPhone X camera while, the HCAL has the resolution of a flip phone cam. :P ^_^

# Hadron Calorimeter

The HCAL is the primary calorimeter that's used for measuring hadron jets, and particles associated with missing energy (MET). These particles that could appear as MET are neutrinos or exotic particles that don't interact with ordinary matter.

The HCAL is divided into several parts. Keeping in mind the cylindrical geometry of the entire CMS detector, the HCAL is split into the barrel region (HB) and the endcap (HE). There is also the outer hadron calorimeter which complements the (HB). This serves as the *tail catcher* and is found behind the CMS magnet that bends charged particles. Then there's the forward calorimeter (HF) which are found behind the HE but at an even more "forward forward" region with $$\eta > 2.8$$.

# Read-out electronics

## Overview
After the particles deposits their energy and induces scintillation light - the read-out electronics will go to work to transmit that information into something that can be stored and analyzed offline.
The read-out electronics has an optical to electrical transducer (another word for transformer) followed by a fast charge-integrating analog-to-digital converter (ADC). We humans basically perceive our world in terms of analog signals, e.g. sound, currents, light. In order to make useful measurements/calculations with these things we "perceive", we need to convert them into countable digital values. This is a good video on it - [ADC-Basics](https://www.youtube.com/watch?v=0y8AD8maAHo).

The digital output of the ADC is then transmitted to the service cavern where the off-detector electronics are located. There signal is used to construct the *trigger primitives* which are sent to the trigger. These are also pipelined or trasmitted in series to the DAQ (data acquisition) if it is accepted by the Level-1 Accept (L1A) trigger (some set of selection criteria).

Next we'll be exploring the the read-out trigger chain, connections to the database and the general framework on the software that allows the machine to communicate with humans.
