---
layout: posts
title: "A Few Discoveries this week"
categories: Dissertation, Life
author: Uzziel Perez
meta: "Markdown Slides with pandoc, Forest nearby, Am not a robot"
math: true
---

### Markdown Slides with pandoc
I've found something really cool. Cool for me. Am not sure if it would be relatable for some. I've just learned this cool way of making "Beamer" presentations without using LATEX!

LATEX is cool but it is cumbersome. I also hate using keynote and powerpoint. But I found Markdown to be an easy way to lay out my thoughts. It's a lot more free flowing. It's just like taking notes. Better than word because it's super easy to type equations and code too!

Initially, I was going to migrate all my presentations to Jupyter slides but I haven't figured out a way to share them without making a public github repo and using [Binder](https://mybinder.org/v2/gh/binder-examples/jupyter-rise/master?filepath=index.ipynb).

Anyway, let's get back to the topic! Making Beamer Slides with Markdown and pandoc.

#### Setup
For starters, I do recommend installing [anaconda](https://sandbox.anaconda.com/) or just installing [pandoc](https://pandoc.org/installing.html)

#### The Markdown File
The slides are separated by single hashes and those also serve as the title. I've linked in the tutorials I've watched.

```
# Slide 1

# Slide 2

- Item
- Another Item
- Etc

# Slide 3

$$ \sum_{a,b} + x \infty $$

# Slide 4

- *This text is in italics*
- **This text is in bold**
- ~~This text has a line through it~~

# Slide 5

![Da Vinci Style CMS Detector](oreach-2009-001.jpg)

# Slide 6

Just want to credit LucidProgramming for the introductory [tutorial](https://www.youtube.com/watch?v=e-HqKSBZOXo).

# Prettification

Thanks to this [prettifying tutorial](https://www.youtube.com/watch?v=dum7q6UXiCE) from Luke Smith, we can add some metadata to make our presentation pretty.

You can find some themes and color themes [here](http://deic.uab.es/~iblanes/beamer_gallery/).

```

#### Styling

You can add some metadata at the top and a separate .tex file to indicate some styles.

*Metadata*
```
---
title:
- Uzzie Presentation
author:
- Uzziel Perez
hyperrefoptions:
- linktoc=all
- pdfwindowui
- pdfpagemode=FullScreen
pagenumbering:
- footer
---
```

*styl.tex file*
```
\addtobeamertemplate{navigation symbols}{}{%
    \usebeamerfont{footline}%
    \usebeamercolor[fg]{footline}%
    \hspace{1em}%
    \insertframenumber/\inserttotalframenumber
}

/* \setbeamertemplate{navigation symbols}{}
\setbeamertemplate{footline}[frame number] */

```

#### Getting the output
To get the output, one can type this in the terminal:

```bash

pandoc -t beamer presentation_sample.md -o output.pdf

```
If you have .tex file to set some stuff:

```bash

pandoc -t beamer --include-in-header=header_pagenrs.tex presentation_sample.md -o output.pdf

```

And the basic output looks like [this](https://drive.google.com/file/d/1c7dTfYyWI109Z0bI0Z8zrbyHUSCgvcet/view?usp=sharing).

### Breaks, work and the Forest nearby

There's a nice forest-y part nearby and I've spent the last two daily walks outside, not using my knee scooter! I'm still a bit slow on the stairs but slowly I'm getting back to my normal walking. ^_^

The past week I was sort of drowning in work (not that anyone put me to it). I just wanted to solve a problem and get a critical amount of work done for me to advance to the next stage of my project. I think I've done it. I am tired. I think I will have to rethink the way I've done things. But one thing I've reconfirmed is that there is great value in focused work where I think about nothing else but the problem at hand. I basically dropped everything else until I finished it. I felt massive relief finishing it, solving problems, and building the code. But sort of felt exhausted in the end. I don't know if this is a necessary kind of thing in the process specially when you are dealing with the nitty-gritty parts of the tailend of your work.

What I plan to do next is to spend the next few days working on detector software with a great degree of focus. The task is clear but the way to get to the finish line is not. So I'd have to do a lot of "exploring" and "playing around" to have a game plan. This project does not have "schedulable tasks". Then when I figure it out I'll code it and test it! Let's see! For schedulable tasks, I'd need to prepare a presentation, do some simulations and also look at some detector images.

I think part of why I got so tired this week (until Thurs) was I spent every waking hour thinking about nothing but the analyzer code. There were two days that I didn't even talk to my room mate. I didn't get to exercise nor walk outside. And I felt robotic. My room mate looked sad too. So I got a little afraid she was thinking that I didn't want to interact with her. Turns out she had a bad toothache. Ha! I gave her paracetamol. Didn't work though.

Also probably didn't help that I ate 5 boxes of Ferrero Rocher this week.. EEEK.
