---
layout: posts
title: "Feynman Diagrams with MadGraph"
categories: Prelim Series
author: Uzziel Perez
meta: "I was trying to see what the NLO corrections were "
math: true
---

## Learning MadGraph

I haven't really sat down to learn [MadGraph](http://madgraph.phys.ucl.ac.be). It's a pretty powerful event generator capable of including next-to-leading order corrections in a process.
The tutorial is pretty good too. If you untar the downloaded package, you can simply run

```bash

./bin/mg5_aMC
MG5_aMC> tutorial
# For NLO stuff
MG5_aMC> tutorial aMCatNLO

```

For our purposes, I only needed to look at the Feynman diagrams being spitted out. You can specify the output folder where they go to. I ran a simple process from the tutorial. The recipe below can be followed as is.

```bash

MG5_aMC> generate p p > e+ ve [QCD]
MG5_aMC> output MY_FIRST_AMCATNLO_RUN
# To display the Feynman diag
MG5_aMC> open index.html

```
The last command is pretty cool because it will show the Feynman diagrams and the information about them.

<img alt="Lumi" src="{{ "/assets/img/NLO_FD.png" width="20" height="20"| prepend: site.baseurl }}" />
