---
layout: posts
title: "Can Kindness Survive in a Mean and Hostile World? (Part III)"
categories: Life
author: Uzziel Perez
meta: "A Christmas Truce, Axelrod and Evolvable Characters"
math: true
---

## Playing with AxelRod's Computer Simulations

I've been talking about some game theory and mentioned briefly about computer simulations on how kindness (or evil) evolves in an iterated prisoner's dilemma. This all started with a guy named Robert Axelrod, a political science professor at the University of Michigan. He got curious about the Cuban missile crisis and how parties could get out of an escalating crisis. One party then could build more bombs, and then the other could build even more and they'd just go to the point of mutual destruction. But then again, if one stops building bombs, one could just be bombed and obliterated. It's a hard game to be in. To understand different scenarios, he imagined an iterated version of prisoner's dilemma where you'll meet the same kind of people again and again. Generally, "you want to cooperate but don't want to get screwed over", Axelrod says.

I listed in a [previous blog](https://uzzielperez.github.io/life/2019/12/03/Can-kindness-survive-in-a-mean-and-hostile-world-p1.html) some of the programs like Tit-fot-Tat and "Massive Retaliatory strike". These programs are made to play against each other 200 times and see who will survive or prosper. The computer programs submitted for the competition are actually open source and you can make your own simulations in your computer! You can check out the documentation [here](https://axelrod.readthedocs.io/en/stable/).

Just for fun, let's look at some basic things we can do with it. First, we can install it through

```bash
pip install axelrod
```
or you can build it from source following the instructions [here](https://axelrod.readthedocs.io/en/stable/tutorials/getting_started/installation.html).

Here's a simple tournament you can run interactively with python or a python script:

```python
import axelrod as axl
players = [axl.Cooperator(), axl.Defector(), axl.TitForTat(), axl.Grudger()]
print (players)
# Run a basic tournament
tournament = axl.Tournament(players)
results = tournament.play()
print (results.ranked_names)
# Result:
# ['Defector', 'Tit For Tat', 'Grudger', 'Cooperator']
```

It's not surprising that the winner in this tournament is the 'Defector' and the 'Cooperator' comes last. The classical Prisoner's dilemma is constructed in such a way that players have more incentives to defect. Tit For Tat comes next. I think there are only 25 rounds here, not 200.

I want to do a bunch of other things with the Axelrod package in [GitHub](https://github.com/uzzielperez/Axelrod). For example, one could explore the different programs, e.g. "Does it manipulate? (mess with the other's source code)", "Does it require a long time to run?". There are also ways to visualize the results of the competition. This I'd like to do a personal project on using javascript maybe. One could also play against different programs through "Human interactions mode". Perhaps the two most interesting things for me to look at are the [Ecological Variant](https://axelrod.readthedocs.io/en/stable/tutorials/further_topics/ecological_variant.html) and the [Evolvable Players](https://axelrod.readthedocs.io/en/stable/tutorials/further_topics/evolvable_players.html). The Ecological variant looks at the evolutionary stability of the different strategies, i.e. these programs can create "babies" and reproduce over time. Pretty cool! And then we can also look at how some players can "mutate". Basically we can simulate natural selection!

So, I've been obsessing about this Axelrod computer simulations because of this (Radiolab podcast)(https://www.wnycstudios.org/podcasts/radiolab/segments/104010-one-good-deed-deserves-another). I've been gushing about this for months! The main question was, can cooperation emerge in this horribly hostile world? This part of the podcast impacted me a lot:

> ** ... the answer was, if you have enough of them so that they have enough chance of meeting each other, they can actually invade and take over the world. Even if the world starts horribly mean... I mean what always sent chills down my spine is that we see this version of morality around the world. You know, be upright, forgiving but retaliatory. I mean, that sounds to me like the Old Testament. It's not turn the other cheek, it's an eye for an eye. But not 10 eyes for an eye. And to think that it's not something that's handed down by our teachers or by God, but that it's something that came from biology, I like that argument personally.** - Steve Strogatz

## A Christmas Truce

I told a friend that the podcasts (including the [other](https://www.wnycstudios.org/podcasts/radiolab/episodes/whats-left-when-youre-right)) doesn't just talk about theoretical math and computer simulation but actual real life examples. And now I think it would be fitting to talk about something that happened on Christmas day in 1914 during the First World War.

Axelrod came across a book called the Live-And-Let-Live System in World War One. One morning, one of the parties just stopped shooting and let the other have breakfast. The other party, I think the Germans, reciprocates. It's just line one of the code for Tit for Tat which says "Be nice first". Moving forward to Christmas Eve, the Germans put up Christmas trees and they lit candles and sung Christmas carols. The British guys and everyone else moved into no-man's land and they exchanged gifts, ate dinner, drank and all the nice things you won't ever imagine in a war.

Some people say that this Christmas Truce didn't happen but there are letters that these soldiers sent back home. There's a movie called "Joyeux Noel" about it that I watched a long time ago. This is the [Christmas Truce scene](https://www.youtube.com/watch?v=hOhrT_li6u8). Probably worth rewatching. 
