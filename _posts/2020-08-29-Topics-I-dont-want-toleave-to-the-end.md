---
layout: posts
title: "Unfolding, Systematic Uncertainties and feeling uncertain"
categories: Physics, Dissertationn
author: Uzziel Perez
meta: "Learning stuff and learning early"
math: true
---


While I am working on the nitty gritty of phase II of the dissertation, I've decided to be more *intentional* about learning various aspects of the analysis. My supervisor already told me to do this but I have been a bit haphazard in actually learning these things. Last night, I dipped my feet back again into this murky aspects. So, here are some notes - a preview of things to come. The idea is, I cannot leave the learning of these relatively foreign concepts to the end or to when I only need them. In fact, for sure, I will need them.

## Unfolding

Particle physics experiments usually collect data on various variables like invariant mass, energy, transverse momentum and so on. The information we get from these variables often undergo a pipeline of algorithms designed to make sure that we're getting the "best" information possible given the fact that detectors are not perfect. When we collect data, we get them in the form of histograms. For a range of values, let's say a particle with energy from 0-100 GeV, we can count how many falls in that range. That range is called a bin, like a container. And then we count how many falls in the 100-200 GeV range and so on. And then we form a histogram.

Each bin has an associated statistical uncertainty in them. Usually $$\sqrt(N)$$, where N is the number of the bin contents (Poisson statistics where each bin are independent). Apart from these random statistical fluctuations you have to consider the finite resolution, the reconstruction efficiency, and the acceptance of the detector. (Reconstruction efficiency - e.g. ratio of how much of the actual photons are being "labeled as photons" over the total number of actual photons. Acceptance - one could think of the spatial or geometrical range or coverage of the detector or the energy range that a detector could actually detect. E.g. detectors have a minimum threshold requirement before they could register some signal). So, the histograms themselves aren't "true representations" of the distributions of the variables we're looking at. So what do we do?

We can have from Monte Carlo (MC) methods an assumption $$f^{model}(t)$$ of the true distribution $$f(t)$$. And from there we can work our way through our expected measured distribution $$g(s)$$ if we know the acceptance, efficiency and so on. It's the other way around, the inverse process of getting the true distribution $$f(t)$$ from the measured $$g(s)$$ that is difficult.

The book *Data Analysis in High Energy Physics: A practical guide to Statistical methods* has a good summary of the things that $$g(s)$$ takes into account:

- *Up-and-down*: The statistical fluctuation from Poisson statistics
- *Sideways smearing*: Potential entries in the bins are missing or some entries that are supposed to be in one bin are moved to another because of reduced efficiency and limited detector acceptance
- *Limited Acceptance and Reduced Efficiency*: The overall height of the histogram is reduced
- *Non-linear Detector response*: The histogram distribution gets shifted in a certain direction on average

If we know these effects, we can "unfold" the true distribution so we can compare directly with theory predictions and other experimental results. I'll write more about this as I get deeper into the details of the work.

## Systematic Uncertainties

When we measure things, let's say with a ruler or a weighing scale, there's a level of uncertainty in the number we are reading. The accuracy (compared to a "true value") of our measurments are limited by how precisely we can read the measurement on a scale. For example, in a ruler, the smallest tick marks are usually 0.1 cm apart. If the tail end of the thing we're measuring is not exactly at the tick mark, then we'd have to *estimate* the value of the hundredth's place in our measurement.

In particle physics, there are a bunch of things to consider and things can be very complex. So this part is usually done at the end of the analysis.

From the same book, here are things to keep in mind as sources of systematic uncertainties: detector efficiencies/acceptances, trigger efficiencies, detector calibrations and resolutions, background, uncertainties in theoretical models and monte carlo simulations, uncertainties in input parameters like luminosity, cross-sections. More difficult to quantify are the following: personal biases and computational and software errors.

# When feeling lost and overwhelmed

I noticed that there are alternating feelings of being lost and perfectly knowing what to do (and just-have-to-sit-down-and-DO-IT feeling). I'm trying to shorten the time of feeling lost. It's frustrating and stressful to be in that state for so long. The so-called "incubation period" in this work is sort of different let's say when you are writing or trying to do a work of art. I can't quite articulate it just yet. Just playing around blindly just doesn't cut it, even if I swear that it is integral to my learning and creativity. But what seems to help recently is some intentional time for solitude and more strenuous physical activity in the form of biking or running. Now that my "hardware" allows me to do so, I believe it's helping me stay in good mental (and physical) shape. Together with this, I find talking to more experienced collaborators -  my adviser, postdocs, HEP friends help clarify the things I need to do in both the immediate and distant future. I don't feel like chewing my foot all the time anymore. I mean these aren't radical concepts. It just takes practice to do be consistent. I am hoping that these things that I've been doing are indeed robust to see me through the end.

Am also learning how to pace myself and communicate when I can deliver my deliverables. I am actually happy that I feel more relaxed and satisfied after some partial task completions. I didn't quite have this skill before but I am learning. As my adviser said, in this line of work "*Research is a marathon, not a sprint*."
