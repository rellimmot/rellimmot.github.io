---
title: "A Sailor Lost at Land"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Engineering
  - Navy
  - Philosophy
---

The ship gets small fast.

You know this intellectually before you sail. You've seen the berthing, you've walked the passageways, you've loaded your kit into a rack barely wider than your shoulders. But you don't really know it until the pier falls away and the coastline drops out of sight, and what you're left with is a steel box surrounded by water in every direction that will kill you if you give it the chance. That's your world now: that narrow berthing, those passageways, that handful of people. Whatever you brought is what you have, and whatever you forgot you do without. The pier is gone.

People romanticize the idea of living on a spaceship: the isolation, the closed system, the hostile void pressing against the hull. I think about this probably more than is healthy, and I've decided I'd be fine with it. I've done it already. Same steel walls, same finite supplies, same total dependence on what you loaded before departure, same hostile nothing outside the hull. The only difference is gravity. Space takes it away. The sea won't let you forget it exists, not for one second of one shift, not even for the cup of coffee you're trying to drink on a deck that hasn't been level since you cleared the channel. A spaceship drifts. A ship insists.

I spent years like this, enough days underway at the Naval Oceanographic Office to accumulate the delusion that I was a sailor rather than a hardware engineer who happened to work on a ship. The ship was piloted by a crew of full-time sailors, each dedicated to their own tasks. They called us shipriders, we were the customers of the ship, and the reason the ship exists. We mapped the sea floor, profiled the salinity and conductivity of the water column, deployed instruments built to survive pressures that find every design shortcut you took. My job was to make sure that hardware worked before it went over the side, and to figure out why it didn't when it came back silent.

<!--more-->

Most days at sea don't make stories. You maintain your instruments. You run your calibrations. You eat when the galley tells you to and sleep when the schedule allows and the horizon is the same flat line it was yesterday and will be tomorrow. The engines drum through the deck plates into your boots and after enough days you stop noticing that vibration you could feel in your eyes when you first set underway, the way you stop hearing your own heartbeat. The ship becomes your body's rhythm: when to wake, when to work, when to eat, when to sleep again. You adapt to the roll, and eventually you forget the ground is supposed to be still.

The thing nobody tells you about going to sea is how clear your head gets. Three meals a day and no choice in the matter. No alcohol. No phone stealing your attention. Our satellite internet ran on a 1.2-second ping and half the web wouldn't load, which turned out to be a gift nobody asked for. Just work, the gym, your books, and more ocean than your eyes can hold. I'd walk laps around the circumference of the ship for exercise, and often I'd sit on a small platform at the tip of the bow and meditate with no timer or goal. The wind overwhelmed every other sound. The sea filled your entire periphery--nothing but blue, deeper than any blue you've ever seen, the kind you can stare into for hours and never once want to look away. The ship bobbed beneath you and for a few minutes you weren't thinking about anything at all. Going to sea was the best thing I ever did for my body and my mind, and I didn't realize that until I came back to land and all the noise returned. This is not the part anyone asks about.

## Three in the Morning

You find out what kind of engineer you are the first time something fails and nobody is coming to help.

On land, failure has a support structure. You call someone. You order a part. You escalate. The whole infrastructure of modern engineering exists to absorb failure and distribute it across enough people and supply chains that no single person ever has to face it alone. You don't even notice this safety net until the first time you're standing in a lab at sea, three in the morning, the ship rolling in long swells, and something on your bench has gone dead and you need it working by sunrise or that part of the mission is scratched, and you realize that everything between you and a solution is you.

No Digi-Key. No McMaster-Carr. No stockroom down the hall. Your supply chain is whatever fit in the boxes you packed before you left the pier, and your engineering team is whoever is on the ship (which, for the hardware, was mostly me).

What this really drills into you is that preparation is the whole game. Every spare you packed, every failure mode you anticipated, every connector you potted with epoxy and every crimp you pull tested is now between you and your data. You either prepared well enough or you didn't and the only thing left after that is improvisation.

## Over the Side

You build the instrument on the bench. You calibrate it. You torture-test it in every way you can think to simulate. You seal it, pot every connector, strain-relieve every cable, tighten every housing. You slide it into a pressure vessel rated for the deepest depths, seal that, and secure the whole assembly into the mooring, an enclosure that will hang out at the sea floor, alone in the dark, doing its job for months or years with nobody watching.

Before it goes over the side, you check everything again. The acoustic release--the only way you'll ever talk to this instrument once it's down. Channels. Encryption settings. The datasheet that says this instrument is on this channel at this location. If any of it doesn't match what you programmed before you sealed the housing, you have sunk months of work to the bottom of the ocean and there is no retrieving it. *Two is one and one is none*. But at some point the redundancy ends and you are left with trust. Trust that the deployment checklist is complete. Trust that what's in the water matches what you'll punch into the transducer.

Then you lug it out to the fantail. The wind hits you. The smell shifts from solder flux to salt. Everyone on deck goes quiet, that keyed-in silence of a deployment when things are dangerous. There's a strong sense of trust you need with your shipmates for over the side operations and they need to trust you too because everybody has a critical job and everybody has the potential to do harm if they can't perform. The A-frame swings the instrument out over the water, you pull the quick release line, *splash* and then it's gone. The anchor drags it down in a graceful arc, the line pays in, the A-frame rises, and there is no trace that your work was ever there.

You go back inside. You drop the transducer over the side and send a chirp into the deep, and you wait for one to come back. The ocean has a lot to say acoustically (other ships, biologics, dolphins, snapping shrimp, the restless noise of the water itself) and your instrument is somewhere down in all of that, either answering or not. The silence between chirps watching the timeout counter tick up the seconds is the longest silence you'll ever sit in.

Sometimes the response comes late. Sometimes the acoustics overwhelm your ability to hear your device. Sometimes the chirp comes back clean and your shoulders drop two inches and you exhale a breath you didn't budget for.

And sometimes the ocean keeps what you gave it. The sea doesn't hold history. It takes what you lower into it and sends back data or silence, and either way the water looks the same.

## Scrounge Engineering

The supply chain at sea isn't a chain at all. It's a box.

Before every cruise I learned to pack like a paranoiac, and for certain deployments the inventory alone took a week. Not just the spares I thought I'd need, but the spares for the spares, and raw materials to fabricate whatever I couldn't anticipate. Rigging. Wire. Epoxy. That homemade tool. Spare connectors in every size. Heat shrink in every gauge. A set of those special cables because if one fails and you don't have another, your mission is over and the ship keeps sailing without your data. You counted every item by hand, checked behind every colleague who helped, and then checked your own work, because what was on the line was too important to trust anyone's count, including yours.

You learn to think three failures deep. Not just *what breaks*, but what breaks *when that breaks*, and what you'll build the fix from when you've burned through your spares. I have repaired instruments with copper scavenged from junction boxes and adhesive that was technically for something else. I have fabricated cable assemblies on a workbench that wouldn't stay level because the sea state had other opinions. You improvise, not because you want to (every engineer prefers the right part and the right procedure), but because the alternative is telling the senior planner that the mission objective is dead because you didn't pack enough connectors.

That kind of constraint rewires your engineering brain permanently. It doesn't make you better in the way a degree or a certification does, it makes you different. You start seeing supply chains as a luxury instead of a given. You start packing for catastrophe in situations where the worst case is a walk down the hall. The paranoia never really leaves, it just finds new things to prepare for.

## Port Call

You notice the change when you come back.

Not right away. The first few days are decompression. The solid ground feels wrong under your feet after weeks of the deck rolling, a rhythmic phantom sway that takes days to fade, as if your body has decided the land is the imposter and the sea is where you belong. You notice the strange luxury of a door you can close and silence you can keep. No gradations of engine and water and steel. But eventually the work starts again, and that's when you realize the sea rearranged something in you for good.

When I left NAVOCEANO and started at Globalstar (satellite communications, a different kind of engineering in a very different lab), the abundance was incredible. Climate-controlled rooms. Racks of RF test equipment with calibration stickers that someone else maintained. A stockroom full of components you could just *use*. Colleagues down the hall who could help troubleshoot. Overnight shipping, if you can believe it. I stood in the stockroom doorway like a shipwreck survivor at a buffet, unable to quite believe that all of this was just *available*, all the time, to everyone, without having to pack it in a Pelican case and carry it up a gangway.

And then I watched people take it for granted and I couldn't understand it. I still don't.

## Land Legs

I am a manufacturing test engineer now. I design test systems for satellite hardware in a climate-controlled lab, far from the water, surrounded by the kind of infrastructure that would have felt like science fiction on a research vessel. I have Digi-Key and McMaster-Carr and a stockroom and colleagues and documentation and a desk that doesn't move. Nobody needs me at three in the morning.

But I still engineer like they might.

I write test code with redundancy and failover built in because the ocean taught me that the first answer isn't always the right one and the system has to survive a wrong one. I design hardware as if it has to work the first time every time, because I spent years in a world where it did. When I look at a system I ask how it will fail, and what happens after that. When I build a test station, I think about the technician who will be standing in front of it on a Saturday night when production is behind and nobody from engineering is answering their phone. I document like someone who knows what it's like to inherit a system with no documentation in a place where you can't call the person who designed it.

People tell me I over-engineer, that I'm a scope-creep addict. They might be right. But I've listened for a chirp from the bottom of the ocean and heard nothing come back, and I will choose over-prepared and slightly ridiculous every single time.

---

I was never really a sailor. I didn't stand watches or navigate or tie the right knots. I was a hardware engineer who worked on a ship, and the distinction matters to people who actually go to sea. But the ocean doesn't care about your job title any more than it cares about your instrument design. What it taught me was consequence: that the world on land, with its stockrooms and overnight shipping and help-a-phone-call-away, is the anomaly. The sea is what things look like when the infrastructure falls away and all that's left is you and your preparation and the knowledge that nobody is coming.

I still feel lost sometimes, in the abundance. I carry the ocean's lessons through a world that doesn't need them most of the time--and then, once in a while, something breaks at three in the morning and the safety net isn't there, and for a moment I'm back on the ship, and I know exactly what to do.

Some lessons don't stay where you learned them.
