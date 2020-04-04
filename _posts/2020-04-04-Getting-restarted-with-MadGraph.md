---
layout: posts
title: "Getting restarted with MadGraph"
categories: Physics Simulation
author: Uzziel Perez
meta: "Simulating"
math: true
---

The main goal of my dissertation is to measure the cross-section of a rare physics process and then later see how well our Monte Carlo methods are able to predict "reality". One of the best Monte Carlo generators out there that are capable of next-to-leading order calculations is a generator called MadGraph. Here I will show how you can run some simple events in your PC. For more advanced but early PhD researchers, I also document how to produce gridpacks for official MC production. Note that for this project, I also use the Sherpa Event Generator. For that I do not have to start from scratch with documentation on using it. If I have time I'll try to share how to use that too. Our research group has been using that for years. (I don't think no one has expertise in using MadGraph in our group and the official documentation is generally terrible for the whole particle physics community.)

I need to learn MadGraph because our "rival" (evil laugh), ATLAS used it for their simulations in an earlier study using 8 TeV data. I need to be able to compare to their results. (Nah, we aren't really rivals. We just try to work independently and compare our results later. CMS and ATLAS are the two general-purpose detectors in the LHC.)

## Getting Started Recipe for PC (Mac OS)

You can download a stable tarfile of the program [here](http://madgraph.phys.ucl.ac.be).

Once you untar, you can go to the directory. In my case it was in the Downloads. You have to have python 2 in your system to run it

```python

cd ~/Downloads/MG5_aMC_v2_7_2
python2 ./bin/mg5_aMC

```

You can follow the rest of the instructions from  my previous [post]( https://uzzielperez.github.io/prelim/series/2019/11/03/MadGraphNLO-Feynman-Diagrams.html) in November.

## Preparing Gridpacks

I found Brendan Regnery's "Adventures with Monte Carlo" in a twiki [page](https://twiki.cern.ch/twiki/bin/view/Sandbox/StandAloneMonteCarloGeneration). Unfortunately it isn't accessible without a CERN log-in. He briefly describes a gridpack as "a tarball (compressed) file that contains a bunch of calculation results stored in away that can be read with cmsdriver."

To produce gridpack you need a bunch of files. More details [here](https://twiki.cern.ch/twiki/bin/viewauth/CMS/QuickGuideMadGraph5aMCatNLO).
* MCProcess_process_card.dat - This is where you declare the process to be generated
* MCProcess_run_card.dat - This is where you define how the generator will run and generate the process with the kinematic cuts
* MCProcess_extramodels.dat - not required
* MCProcess_customizecards.dat - not required for SM lagrangians

The [old documentation](https://twiki.cern.ch/twiki/bin/view/CMS/MadGraphFall13Production#Preparation_of_the_cards) gives a more verbose description of each card.

### Quick Recipe for Gridpack production

```python

git clone git@github.com:cms-sw/genproductions.git genproductions
cd genproductions/bin/MadGraph5_aMCatNLO/
./gridpack_generation.sh <name of process card without _proc_card.dat> <folder containing cards relative to current location>

```
### A Quick look at sample cards

Before producing the gridpacks, we'll have to know, or I'll have to know what should go in the process and run cards. For now, here are some links to some examples:
* https://github.com/cms-sw/genproductions/blob/master/bin/MadGraph5_aMCatNLO/cards/examples/wplustest_4f_NLO/wplustest_4f_NLO_run_card.dat
* https://github.com/cms-sw/genproductions/blob/master/bin/MadGraph5_aMCatNLO/cards/examples/wplustest_4f_NLO/wplustest_4f_NLO_proc_card.dat

I'll be updating this post as I make progress in figuring things out.

<!-- Accessible only with a CERN account.
https://twiki.cern.ch/twiki/bin/view/Main/YuanChaoMCprod15
https://twiki.cern.ch/twiki/bin/view/Sandbox/StandAloneMonteCarloGeneration -->
