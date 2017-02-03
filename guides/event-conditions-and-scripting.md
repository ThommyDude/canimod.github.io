---
layout: default
title: Conditions and scripting for events
intro: >
    This page lists all known condtions(triggers) and scripting commandsds currently known.
    <p class="warning">
    This list may be incomplete. <a href="https://github.com/Pathoschild/canimod.github.io#ways-to-contribute">Feel free to add more</a>
    if you have found any triggers or commands that are not listed.
    </p>
---

## Intro

### How events are made
Events are stored in Content\Data\Event\(room_name).xnb, to learn more about what to do with xnb files please check [creating an XNB mod](creating-an-xnb-mod) because we will not be covering that here.

When you extract one of the xnb files you instead get a .yaml you can edit in, for example, Notepad++.
When opened you'll see alot of information, but the important part(s) are all under the ```content:  #!Dictionary<String,String>```.

As an example we'll look at one of the events in the Beach.xnb(.yaml) file and look at the following event:
```yaml
739330/t 600 1710/j 1: "ocean/-1000 -1000/farmer 28 35 1 Willy 44 35 1/removeQuest 13/addMailReceived NOQUEST_13/skippable/animate Willy false true 250 28 29 30 31/viewport 44 35 true/move farmer 7 0 1/playSound seagulls/move farmer 7 0 1/pause 500/playSound seagulls/pause 1000/playSound seagulls/speak Willy \"Ahoy there, son.$u^Ahoy there, miss.$u#$b#Heard there was a newcomer in town... Good to finally meet ya.$u\"/pause 500/playSound seagulls/pause 1000/stopAnimation Willy/playSound dwop/faceDirection Willy 2 true/pause 50/faceDirection Willy 3/pause 1000/speak Willy \"Ah... I'm still tryin' to unwind from a month out on the salty seas...$h#$b#It was a big haul! I sold a lot of good fish.#$b#Finally saved enough to buy me a new rod.$h\"/move Willy -1 0 3/pause 1000/speak Willy \"Here, I want you to have my old fishing rod.$h#$b#It's important to me that the art o' fishing stays alive. And hey, maybe you'll buy somethin' from the shop once in a while.$h\"/pause 1000/playSound seagulls/pause 500/faceDirection farmer 2/itemAboveHead rod/pause 3300/awardFestivalPrize rod/faceDirection farmer 2/pause 1000/playSound seagulls/move Willy 0 1 2/pause 1000/showFrame Willy 24/pause 1000/speak Willy \"There's good water here in the valley. All kinds o' fish.\"/pause 1000/faceDirection Willy 3/speak Willy \"Oh yeah. My shop's back open now, so come by if you need supplies.$h#$b#I'll also buy anything you catch.#$b#'If it smells, it sells'. Heh heh. That's what my ol' Pappy used to say, anyway.$h\"/pause 500/playSound seagulls/pause 500/move farmer 0 1 2/pause 1000/pause 500/animate Willy false true 250 28 29 30 31/viewport move 1 0 5500/pause 1500/playSound seagulls/pause 1500/playSound seagulls/pause 2000/end position 42 36" #!String
```
Alright, that's a giant long mess, let's look at it in a way that makes it all a bit easier:
```yaml
739330/t 600 1710/j 1
```
This is the part in front of the ```:``` which are the conditions that cause the event to trigger when they are true. However the very first one ```739330``` is actually the Event ID.
Every event NEEDS a unique ID otherwise there will be conflicts and then none of the events with the same ID will work correctly, or at all.
