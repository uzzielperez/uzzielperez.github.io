---
layout: posts
title: "Clean Code"
categories: Physics
author: Uzziel Perez
meta: "The importance of having clean code"
math: true
---

I have began rereading a book called "Clean Code" by Robert Martin. I've been a little stuck this week physics-wise, so I've decided to organize my coding infrastructure in a certain way. I try to think of it as growing a bonsai tree or just growing a manicured beautiful-looking plant. It will grow organically but it wouldn't grow all over the place that it (the code) would be rendered useless or too troublesome/confusing to use.

I made the structure look like this.

```bash
├── Analyzers                # From MiniAOD/AOD to Ntuples
├── AnalysesTools            # From Ntuples to Histograms to Pretty Plots
    ├── makeClass               # make raw histograms
    ├── makePrettyPlots         # make histograms pretty with labels and stories
    ├── etc                     # other tools
├── LICENSE
└── README.md
```


And the makePrettyPlots...

```bash
.
    ├── ...
    ├── makePrettyPlots
    │   ├── README.md    # usage
    │   ├── bin          # executables
    │   ├── interface    # reusable stuff
    │   ├── data
    │   ├── test          # Unit tests
    │   ├── scripts       # miscellaneous scripts
    │   └── python        # python plotters or scripts
    └── ...
.
```

The idea is I want a simple interface where I can call different functions to do things that I want, like do this plot, or show that comparison etc. I pretty much have an idea of how I want it to look like since I've some experience working on a previous analysis. I have some idea on the good practices in the old code that I want to carry here in this project. And then I have some idea on how I'd like it to work based on what I want. I kind of felt happy doing this because I felt "creative"! I felt like I am making something! :D

The book is a wonderful read, just like the "Zen Programmer" book which I've learned a lot from. It gives some general guidelines like provide meaningful, intention-revealing names (for functions, variables, etc.), practice routine cleaning up ( break up functions that are large, eliminate duplication) and so on. What I also like is the humility of the author that "clean code" is subjective and that they're not somehow "right" in any absolute sense. They're just giving some techniques and teaching that they practice in their art, that allowed to them to enjoy some benefits.

Perhaps one of the best descriptions of what constitutes as clean code was suggested by Grady Booch. "Clean Code reads like well-written prose. Clean code never obscures the designer's intent but rather is full of crisp abstractions and straightforward lines of control." The author then asked to think about a really good book one has read. "You saw the characters, you heard the sounds, you experienced the pathos and the humor".

I've been working a lot with other people's code for the past year and I miss writing my own code. It can also be very hard to read other people's code. It can sometimes take me weeks just to understand what some code does and then fix it to suit my needs. Before you can write new code, you've got to learn what's already written.

I'm a little bit embarrassed about the mess I've created in this [repository](https://github.com/uzzielperez/Analyses) but I'm quite happy that I've just been generous to myself. I allowed myself to just commit code that I thought was kinda fun to make, but not that clean since 2018. And now I'm quite pleased that I can share some of the solutions I've had in this repo to some other folks too.

I was hoping to write some physics stuff per week but nothing has crystallized yet. Maybe I'll figure something out next time. Just being intentional about writing and talking about my work, would hopefully be pretty useful for the actual dissertation writing stage. And perhaps give me motivation to make consistent progress until I finish a major section of the whole work in the next few months.
