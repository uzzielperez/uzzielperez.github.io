---
layout: posts
title: "HCAL Data flow"
categories: Physics
author: Uzziel Perez
meta: "More Clarity"
math: true
---

I've probably gone through the HCAL technical papers and slides so many times but I think my brain doesn't have a clear simple representation of the system in my head.
But this week, I had a moment of clarity after speaking with our postdoc, about what actually happens with the code that I am working on. My task was to measure how much time my new code adds to
the "configuration time", which is like "loading time" in a console for some particular game settings. It didn't add too much, which was good. But I found something mysterious.

I thought that if I disable the registers in the ngCCM machine that my code would also stop writing the register values. Therefore, if the registers are disabled, then it wouldn't add to the configuration time.
But I didn't see that! I still saw the configuration time was longer. I had this misunderstanding, that I thought I knew in theory all ready but didn't quite connect.

So it turns out that during configuration, my code only tells some machine, called the "ngCCM server" to write this or that values depending on how it is programmed. *It's only going to do what it was told to do so*. And then it's a whole other step where the ngCCM server (where you can disable the registers), will write the values to the Front End (I hope I understood this right).

There are many times I feel confused and don't understand things. And it takes a while for me to have some more clarity! I usually do this by drawing stuff, talking and asking questions to people who knows more than I do, walking, reading and thinking. Or sometimes, I just go to sleep. :P Confusion (and feeling dumb), is something that is commonplace in my line of work. But the clarity one gets, the freeing up of mental bandwidth that occurs when one figures something out, is one of the feelings that I live for! :D
