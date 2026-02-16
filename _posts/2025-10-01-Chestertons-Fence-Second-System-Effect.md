---
title: "Chesterton's Fence by way of Sisyphus: Musings on Reinvention"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Engineering
  - Software
  - Philosophy
  - Systems Design
  - Manufacturing
---

There's something beautifully human about a pattern I keep seeing in engineering: we encounter an existing solution and immediately think "This is primitive, inelegant, clearly built by people who didn't understand the problem space." So we architect our masterpiece - clean abstractions, modern patterns, everything the original lacked.

Recently, in a project presentation, I saw this pattern play out and immediately grinned. RF shield clips—the exact approach we'd fought for in the original design and lost—were being proposed again, this time over the shield frame we'd settled on. We had always used clips, finicky but modular—we've gone full circle. I thought of two classics, [Chesterton's Fence](https://en.wikipedia.org/wiki/G._K._Chesterton#Chesterton's_fence) and Sisyphus. Call it a "Chesterton's Fence by way of Sisyphus" journey - where you tear down the fence, build an elaborate gate system, add biometric scanners, implement a cloud-based access control platform, and then six months later you're back to... a fence. But now you *understand* why it's a fence.

<!--more-->

It's reengineering the Legacy Manufacturing Test Rack and coming full circle in our solution to something which resembles… the Legacy Manufacturing Test Rack. All the legacy racks needed were some maintenance and a refresh. I strive to get us back to using them, but the *never-going-to-happen* we'll always chase is that there aren't enough of them — and that puts the whole concept of having more on a pedestal. There is no better time than tomorrow to have more of them made. Ultimately we would have spent less time, effort, and money having more of them built, but I don't want to harp too harshly on that.

As we iteratively pursue more new solutions, the reality of reinvention starts its slow, methodical assault. Edge case by edge case, you find yourself adding the exact "inelegant" compromises you scorned. That weird validation hook? Turns out it prevents a catastrophic failure mode. That seemingly redundant process? It's the load-bearing wall of the entire system.

## The Second System Effect

The [Second System Effect](https://en.wikipedia.org/wiki/Second-system_effect) - we build the next iteration to be everything the first system should have been only to discover the first system was everything it needed to be. Fred Brooks the author of *The Mythical Man-Month* ([The Second System Effect: Page 53](https://wiki.c2.com/?SecondSystemEffect)) states it well in Figure 1.

![Self-Discipline—The Second-System Effect](/assets/images/posts/chestertons-fence/SecondSystemEffect.png){: .align-right}

## The Trailing Edge is the Bleeding Edge

Sometimes the boring, proven solution that everyone wants to revolutionize is boring precisely because it works. It's survived the gauntlet of production. Your clever improvement hasn't.

Of course, sometimes you do improve things. But more often, you end up with what we can call *reinvention regression* where you spent six months traveling in a circle, except now you're dizzy and behind schedule. But hey, at least you now have a visceral understanding of why that ugly hack in line 47 exists. Alas, sometimes these critical hacks really do hold everything together and we should all consider the chaotic intricacy of the legacy code for examples of this.

That Sisyphus article says it like *"The hack you put in will stay in production 'til after we die."* That's the truth. Strive to do it right the first time because there will always be something higher priority than going back and refactoring your old code to do it the way you wanted to in the beginning but didn't have enough time. Similarly for writing comments and documentation as you code. That disgusting workaround you added at 11pm to unlock production may exist years later and sometimes that is okay.

Code is imperfect because we are imperfect. Elegant code is what we write before we meet actual hardware. You need to think about that last sentence in the context of my LabVIEW mentor who quit our team this year. My mentor's magnum opus — the LVOOP we built together — had very little error correction and counted on our hardware and the test instruments behaving like perfect robots when we all know they are bad robots. There was little to no logic, loops, or workaround and all attempts by me to add it were rejected outright. Find the bug. Sometimes we can't squish a bug if it's locked in a black box.

Compare the code from now to then and it's the difference between writing the elegant optimal code and the code you get after you meet the hardware, after every AT command behaves differently, after it decides to reboot and throw unexpected responses, after you run into real manufacturing defects. *"Andon systems be damned!"* I imagine they would have said. Now we must face the reality that what holds our systems back the most sometimes is the lack thereof.

## Wisdom in Recognizing Convergence

Sometimes we spend hours refactoring legacy code we don't think works only to discover the minorly broken thing and that in the original system my predecessor had already fought this exact battle and lost as well. Those weird delays, those seemingly redundant checks, those were their fight with reality. We can only shake our heads and wish they left a comment about why we need 3.7 seconds right there in the sequence. Before we refactor ugly code we need to ask *"what hurt you?"* because something probably did and it's probably for a good reason.

The real wisdom isn't avoiding reinvention - it's recognizing when you're converging back to the original solution and having the humility to say *"oh, THAT's why they did it that way"* instead of stubbornly pushing forward with your elegant-but-doomed alternative.

---

These musings contain no actionable insight but rather a retrospective on respecting the why and how we came to have the systems that we have. I believe to leave everything how it is would be to lack a creative drive, and without a creative drive we may still be engineers, but perhaps not the best developers we could be.

Where does that leave us? Somewhere between reverence and rebellion, methinks. The answer isn't to stop pushing the boulder, it's to ask better questions before we start.
