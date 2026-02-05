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

## [Download the game off the repository.](https://github.com/The-Ondeveloper/FingerPistols)

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

Outside of the finger pistols mechanics, I developed several other abilities for the player to help them get around.
The player has a double jump, an uppercut, and a charge up punch that launches them in the direction they are facing.
These abilities are designed to be usuable once each time the player leaves the ground, however, 
interacting with certain objects in the environment can refresh abilities mid-jump allowing the player to gain some impressive airtime.
I wanted a wide range of abilities to allow the player to mix up their movements and combo their abilities, 
creating a satisfying level of skill expression and creativity in how player's approach a level; in combination with environmental interactions, players can beat most levels
while barely touching the ground which gives the game a unique sense of speed and flow. 

## Score system and the user interface

Every good game built for speedrunning comes with some kind of score system, for this game I wanted the score system to be weighted between both
how quick you can beat a level and how stylishly you can do it. The game awards you a rank based on how highly you score, and your score is multiplied at the end
of a level based on your time and highest combo. A combo in this game is how many 'interactions' you can pull off mid-air, 
every ability and object you interact with without touching the ground increases your combo multiplier. You also gain points by travelling in mid-air and interacting
with objects, everytime you touch the ground your current combo multiplier and 'combo score' gets cashed-in and added to the total score.

To represent the score system in game, I designed the UI to display the total score as well as the current combo multiplier and current combo score.
I also decided it would be a nice visual flair if there was a brief pop-up when you interact with an object, this shows information designed to
help players learn about an object by displaying it's name and a little icon, it also displays how many points you got by interacting with the object.
I also designed icons for all of the player's abilities to help player's keep track of what abilities they can still use during a jump. 
I wanted the UI to be as informative as possible without relying on text so that players can easily keep track of information they need on the fly,
such as available abilities, as well as helping make the various interactable objects in the game more intuitive to understand.

## Designing the levels

My philosophy behind level design was that every level should be short and sweet, which makes an individual level easier to learn for speedrunning, 
and less punishing when you make a mistake. I also took inspiration from the design philosophy of Nintendo games such as Super Mario Wonder,
where every level is kept interesting by introducing a new gimmick for each time. 
In my game the level gimmick is defined by the interactable object introduced in that level. 
For example, the first level after the tutorial introduces jump pads and is built around using them to ascend a tall tower,
meanwhile the second level introduces boost rings and is built around using them to fly through a race track.
The second level still features jump pads but revolves more heavily around boost rings as it's special *gimmick*.

## Additional viewing

### Finger Pistols playthrough

[![Link to a playthrough of Finger Pistols](https://img.youtube.com/vi/8FUguKl-LaQ/0.jpg)](https://www.youtube.com/watch?v=8FUguKl-LaQ)

### Finger Pistols Test Level Showcase

[![Link to a Test level showcase of Finger Pistols](https://img.youtube.com/vi/TTVkor2Kyg4/0.jpg)](https://www.youtube.com/watch?v=TTVkor2Kyg4)








