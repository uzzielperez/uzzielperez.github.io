---
layout: posts
title: "A new approach to work"
categories: HEP Theory
author: Uzziel Perez
meta: "PhD Research"
math: true
---

For the past 10+ years I've mostly coded with python. I love python. It's easy to learn and easy to use. You can write in a few lines what would take several more lines in C++. So I've always plotted and wrote my scripts in python. I am two months away from my Preliminary Examination - the final exam before I become called a *PhD candidate*.

I have been making slow but steady progress over the past month. This past week, things have been accelerating. I've been meeting everyday with Conor, my adviser, to talk physics and talk about some ROOT tricks. I think that I have been paying too much attention to the elegance of my code that I have neglected the physics aspect of the research. Not only am I not trying to answer physics questions, I am also not good at asking the right questions. Hopefully, I can improve in this aspect.

The way we comb through data is through a code base called a ExoDiphoton Analyzer. The analyzer I am using is a modified version of my senior's PhD work, only I had to put a 3rd photon selector. When we run the analyzer on some intermediate data, we get what we call "Ntuples". Now, the way our code base writes out the information in the ntuples is something that I don't know how to directly handle with Python. Only recently did I finally accept that doing it with a C++ macro would be a lot faster. I am also learning a lot of ROOT tricks! I still think that ROOT is sometimes a pain in the butt!

Learning how to do things interactively through ROOT helped us test ideas much more rapidly. In that case, ROOT is amazing. I am also happy that most ROOT installations ships with a "linker" to jupyter notebooks. Not sure if that's the correct term but I like the interactivity. Shorter time-to-physics!


Last Note:

I've also been using the pretty nifty [ATOM](https://atom.io) text editor for my work recently, whether I'm connected through the Fermilab cluster or just working on my Desktop. Since I am also trying to produce quick results, my code is not overengineered. 
