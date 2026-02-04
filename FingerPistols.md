---
layout: default
title: "Finger Pistols"
permalink: /FingerPistols
---

# Finger Pistols

## Demo Trailer

[![link to Finger Pistols trailer video](https://img.youtube.com/vi/R2UXdSEtlkQ/0.jpg)](https://youtu.be/R2UXdSEtlkQ)

## About

Finger Pistols is a solo project created for university, where the brief was to create a vertical slice of any game idea we wanted.
The project was made in Unreal Engine 5.

I had the idea for a speedrunning platformer, in a similar vein as Neon White,
with the gimmick of being able interact with objects in the environment without having to *physically* touch them via shooting them with your **finger pistols**.
For example, you could shoot a jump pad to gain a height boost, a speed ring to leap forward, a grapple point to swing from it, etc.
I got the concept for the finger pistols themselves from the character Doomfist from Overwatch, which also inspired the characters moveset,
including an uppercut and a punch that boosts you forward.

## Developing remote interactions with the finger pistols

The most important mechanic of Finger Pistols unique gameplay is the ability to remotely interact with objects and gain their affects by shooting them.

Every player projectile is kept in an object pool attached to the player character, when a projectile is initialised it is told the player character is its parent.
This is important as when the projectile hits something it sends an interface and passes a reference to the player character to whatever it hits;
if that object is interactable, then it will implement the interface and cause somekind of affect on the player character.

I decided to make the projectile somewhat slow to add a delay when shooting objects further away, 
this descision was made to balance the game's difficulty by adding more risk to shooting objects further and more punishment for missing a shot.
The slight delay also added a nice unique game feel as the player can essentially "queue" interactions by shooting one object while preparing their next action
or shooting at a completely different object.
 
Due to the ability to remotely interact with objects some balancing descisions had to be made, for example, most obstacles have quite a long cooldown before they can
be interacted with again, which was necessary to prevent features such as being able to infinetly fly using a single jump pad.

## Developing movement mechanics

