---
layout: posts
title: "HCAL Data flow and Project Update"
categories: Physics
author: Uzziel Perez
meta: "More Clarity and learning from Mistakes"
math: true
---

I've probably gone through the HCAL technical papers and slides so many times but I think my brain doesn't have a clear and simple representation of the system in my head. But this week, I had a moment of clarity after speaking with our postdoc, about what actually happens with the code that I am working on (at least a small part of it).  My task was to measure how much time my new code adds to
the "configuration time", which is like "loading time" in a console for some particular game settings. It didn't add too much, which was good. But I found something mysterious.

I thought that if I disable the registers in the ngCCM machine that my code would also stop writing the register values. Therefore, if the registers are disabled, then it wouldn't add to the configuration time.
But I didn't see that! I still saw the configuration time was longer. I had this fundamental misunderstanding, that I thought I knew in theory all ready but didn't quite connect.

So it turns out that during configuration, my code only tells some machine, called the "ngCCM server" to write values depending on how it is programmed. *It's only going to do what it was told to do so*. And then it's a whole other step where the ngCCM server (where you can disable the registers), communicates with the ngFrontEnds to actually write the register values. It's apparently another set of codebase that is maintained by someone else in our team.

There are many times I feel confused and don't understand things. And it takes a while for me to have some more clarity! I usually do this by drawing stuff, talking and asking questions to people who knows more than I do, walking, reading and thinking. Or sometimes, I just go to sleep. :P Confusion (and feeling dumb), is something that is commonplace at work. But the clarity one gets, the freeing up of mental bandwidth that occurs when one figures something out, is one of the feelings that I live for! :D

We're now moving on to another stage of the project where we move from technical implementation to coordinating with the physics end users of the project. That's going to take some time again. But it's really nice to just go from "I don't know what I'm doing" and "I don't know how to start", to "we've made it work"! And it also feels nice to be working with people who support your learning even if you don't know a lot in the begginning. And I appreciate the time investment they made to help me learn about the system. Time investment is really valuable.

I definitely had times that I had to muster the courage to ask questions and look dumb. And I also had times when I screwed the code, the system and made mistakes were embarrassing. Like, one time I actually screwed up the actual detector system at that BIG detector. The good thing it wasn't a high-stakes situation, i.e. not on data taking with stable beams. I think I've been accustomed to failure. I'm not desensitized by the negative feelings associated with it. It's just that I know when I fail, I have to be mindful about getting it right the next time, otherwise, it means I have not learned. And if I haven't learned, I will just keep repeating the same mistakes. Of course, the embarrassment and shame of failure is not an easy thing to deal with at the moment itself. But when I got more used to "mindful failing", I less likely overidentify and attach my self-worth to a failure. It's easier to pick myself up, sit down and ask myself "What have I done and how could I have done this better?" Goes with everything in life.

Anyway, I can focus on physics this week!
