---
layout: posts
title: "Fake Rate Implementation"
categories: Physics, Dissertationn
author: Uzziel Perez
meta: "Going through old code and making my own"
math: true
---

It's been three or four months since I set out to work on the fake rate method. I had encountered several challenges regarding what samples to begin working on, understanding the code infrastructure that's already there, and how I could use them for my own work. And am also figuring out the things I need to start out from scratch.
Probably took me 2 months of being "lost" and just going around in circles reading and playing around with stuff. It was only in the last two weeks, when I had the chance to fully focus on this that I had made some strides in this phase of the project. It probably helped a lot that I also feel that I am in great mental shape now. I expect to work on this for a couple of months more. That's being generous.

So the old code had several components. At the very top level there is the Ntuplizer code for the diphoton. I didn't have to touch that but I had some trouble running them because CMSSW had to be set up a certain way. Then there are the template producers that gives you the histograms for Fake Objects, Real/Signal Objects, numerator (objects that pass the ID - which includes jets and real photons), and the denominator (objects which pass a looser ID where one variable cut is inverted). So that one, I went through a little bit because I didn't know what was going on in the code. They actually run and produce the files you need, but things are not as seamless because you have to find the files in the right directory. So am working with our postdoc to make the running on samples a little more hands-free.

Finally, the part that I am most responsible for is the fitting code. The first order task (which I finally finished!), was to replicate some of the plots in the old analysis note and add the lost features that was uncommitted in GitHub. The work itself, spearheaded by my adviser and my friend Andrew was published in [Phys. Rev](https://arxiv.org/abs/1809.00327). I am now just adding a few more features so that things are set up such that pretty plots can be made with a smoother workflow.

# Some Physics Notes
I'm taking a lot of time with the programming aspects of the study but I mustn't forget the physics part. Much of these notes are derived from my discussion with my adviser.

First, there are things we have to make clear. When doing the closure test, we are treating Monte Carlo samples as if they are data. We're just applying the exact method that we're applying on actual data to a bunch of Monte Carlo Samples. Note that in the real data, we don't have a way to 100 percent tell apart which is a real photon and which is a jet/fake. But... in Monte Carlo... we could tell them apart because, it's a simulation and we can trace back the history and parents of the photons/objects in the final state. Because we have access to its history, we can label them as fake or real.

We are applying a template fitting method. Last time I talked about the shower shape variable, sigmaietaieta that tells about how wide the splash an object makes in the detector (ECAL). For real photons, the splash isn't quite large so you can expect a histogram peaking below some value. Fake photons are skewed towards larger values of sigmaietieta. The numerator, like what I said earlier, is a combination of both jets and photons so you could superimpose the real and fake templates and it would somehow look like the numerator template.

An important thing to note is that these templates aren't perfect. So you would expect some bias in the results. The best way we can minimize this bias is to prepare the templates with objects in a particular charged hadron isolation sideband. Charged Hadron Isolation is another one of those photon ID variables that can help us discriminate photons from jets. The more surrounded an object is by charged hadrons, the more likely it's not a photon!

So what's with this sideband thing? So people who've studied and prepared a suitable photon ID found that real photons would most likely have a Charged Hadron Isolation (chIso) value of no greater than 5. So 0 < chIso < 5 is the signal region. The thing is, the variables sigmaietaieta and chIso are correlated for jet objects. They are both affected by the fragmentation process. The larger the value of sigmaietaieta, the more unlikely it is to be a photon and therefore the more unlikely it is to fall within the chIso signal region. Conversely, if the object falls farther from the 0 < chIso < 5  signal region band, the more likely it is that it has a larger value of sigmaietaieta.

The best thing we could do to minimize the bias is to prepare the sigmaietaieta template falling within the sideband 5 < chIso < 10. It's close enough to the signal region, but still outside, so we know they contain mostly fake stuff but still probably has some "real photon contamination".

So, things will be a little more clearer in the coming weeks or so. I will continue to write my notes and learnings. Good practice for the actual dissertation writing.
