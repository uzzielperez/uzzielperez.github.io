---
layout: posts
title: "Some Dummy's Guide To Limits Setting written by a dummy"
categories: Physics
author: Uzziel Perez
meta: "Before I forget"
math: true
----

I'd like to continue my streak of dumminess by trying to write a dummy's guide to Limits setting (perhaps the first of many, perhaps)!
So we're trying to figure out which points in the parameter space are to be excluded for a certain Beyond Standard Physics Model.
I've been reading through books and lectures and I couldn't quite understand them myself (like a dummy hehe!). So with the help of my adviser, we walked through some concrete examples on how to know which "hypotheses" we could reject with some level of confidence.


So let's say we have zero background as our null hypothesis. We have several alternative hypotheses corresponding to different points in the parameter space of the model. Each of the different model points predicts different numbers of events in the signal region when we look at a certain variable like the invariant mass of two photons. The distribution of the invariant mass of the photons are poisson distributions


```
root [0] TMath::Poisson(0, 1)
(double) 0.36787944
root [1] TMath::Poisson(0, 2.4)
(double) 0.090717953
root [2] TMath::Poisson(0, 3)
(double) 0.049787068
root [3] TMath::Poisson(0, 4)
(double) 0.018315639
root [4] TMath::Poisson(0, 5)
(double) 0.0067379470
root [5] TMath::Poisson(0, 6)
```
