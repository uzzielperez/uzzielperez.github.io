---
layout: posts
title: "MadGraph Production"
categories: Physics Simulation
author: Uzziel Perez
meta: "Standalone Production"
math: true
---


It took a while before I got to return to doing MadGraph. I dipped my feet into it by writing this [documentation](https://uzzielperez.github.io/physics/simulation/2020/04/04/Getting-restarted-with-MadGraph.html) which proved to be extremely helpful for myself after not doing it for a long time. I don't really super have to do this because I've been doing Sherpa but it's good to validate our samples with another event generator. I've also validated my signal sample by comparing the signal distributions at LO and NLO, all of them normalized with the proper cross-sections. I figured it would be good to document this in more detail while the gridpack production is running.  

Everything from here on assumes that you are working within the CMSSW framework. I have decided to both submit a request that goes through central production and simultaneously make my own samples going through the full chain that includes detector simulation. Why do I need both? I need the central production for a larger dataset so I have also have enough statistics. My results cannot be published if my samples do not go through this step. Since this will take months, I need to do some quick studies and prototyping with a smaller number of events. So I'm going to have to go through this too. 

### Quick Recipe for Gridpack production

I'm just picking out the basic instructions from this [twiki page](https://twiki.cern.ch/twiki/bin/viewauth/CMS/QuickGuideMadGraph5aMCatNLO).

```python

git clone git@github.com:cms-sw/genproductions.git genproductions
cd genproductions/bin/MadGraph5_aMCatNLO/
./gridpack_generation.sh <name of process card without _proc_card.dat> <folder containing cards relative to current location>

```

For example 

```python 

./gridpack_generation.sh wplustest_4f_NLO cards/examples/wplustest_4f_NLO

```

You can do the gridpack generation on condor clusters and via CMS connect. But for our purposes the one above should be sufficient. 

### Let's Produce Events!

After generating the gridpack, you now have the ingredients or code that are needed to produce events. 

```python

cmsrel CMSSW_X_Y_Z # same as gridpack gen release 
cd CMSSW_X_Y_Z/src
cmsenv

```

```python

tar -xavf <path of gridpack creation>/wplustest_LO_tarball.tar.xz
bash 
./runcmsgrid.sh <NEvents> <RandomSeed> <NumberOfCPUs>

```

I will discuss about Pythia8 Hadronization when I'm done with Event generation.  

*PADAYON!* :) 

