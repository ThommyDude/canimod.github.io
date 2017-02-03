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
