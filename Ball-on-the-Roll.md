---
layout: default
title: Ball on the Roll
permalink: /Ball-on-the-Roll
---

# Ball on the Roll

## Demo Playthrough video

[![Link to the Demo playthrough video.](https://img.youtube.com/vi/CV5w6uu1tZI/0.jpg)](https://youtu.be/CV5w6uu1tZI)

## About

Ball on the Roll is a solo project for university, the goal of the module was to produce a short demo of a game made in C++ and UE5.
This game is based of a small project I did over summer, that attempted to recreate the physics of the game Super Monkey Ball. 
While working on that project I had an idea for my own spin on the ball rolling genre of games. This idea, which I ended up basing this project on, was for a game
where you navigate the ball through a labyrinth style level, using a floating hand that can also interact with the environment
to help the ball get to the goal. 

The main mechanic of the game is the ability to pick up and move around various physics objects with the floating hand, which you control with the mouse.
Of course there's the player ball which can be moved by dragging it with the hand, but there are also projectiles that the player can drag to move them out the
way of the ball's way. The game also features several additional mechanics, such as multiple hand types and collectibles that add some extra depth to what can
be done with the level design.

## [Download the game off the repository.](https://github.com/The-Ondeveloper/Ball_on_the_roll)

## Making the Ball Roll

To define the logic for objects that can be picked up, I created a 'grabbable object' component and corresponding interface that allows the player hand
to tell an object has been picked up. When an object has been picked up, it is allowed to define what happens to it when the player is holding on to it; 
both the player ball and projectiles use a 'grabbable physics object' component, which causes them to slow down when the player holds still,
and move when the player drags in a direction.

I wanted it to be flexible what happens to an object when it's grabbed to allow the possibility for a variety of different objects,
in the event of this project being expanded into a bigger game, for example, levers and handles to open doors would need their own behaviour to move properly
when 'picked up'.

![Gameplay of picking up various objects.](Assets/BotRGameplay.gif)

When the hand successfully picks up an object, it's only given very limited data about the object that it needs to know, 
such as the grip strength the object has, but it never actually learns what object it's grabbing, which allows it to stay decoupled from the environment.

Grabbable objects are still allowed to have their own logic seperate from their role as something for the player to pick up, 
an example of this is the player ball, which has its own health stat -reprsented by the blue ball on the ui- 
and drives the flow of gameplay, being able to end the level by reaching the goal, and causing the level to reset when it is destroyed. 
The player ball also has the unique ability to pick up collectibles, including coins and new hands for the player to equip.


## Developing the hands

The game features the ability to swap between multiple equippable hands, the demo features a finger pistols hand [(Using the same assets as Finger Pistols)](https://The-Ondeveloper.github.io/FingerPistols)
that shoots a projectile that can destroy turrets and breakable walls, this ability replaces the default hands ability to pick up objects. 
All hands are derived from the same base class, which allows all unlocked hands to be stored in the same pool on the player controller, 
meaning the controller can change which hand is being used on the fly. The player controller uses interfaces to give input to the currently equipped hand,
this means that all hands can share the same input bindings for their own unique abilities.

All hands have a 'health stat' represented by a red hand on the UI. The default hand uses the health stat when grabbing an object that causes damage to it, 
such as the burning projectiles, and is forced to let go when it runs out of health. Meanwhile, the finger pistols hand uses it as more of an *ammo count*,
when you use too many projectiles in a row, you run out of 'health' and are forced to stop shooting for a while.

## Developing the obstacles

Across the level, there are several turrets that fire projectiles in an attempt to destroy the player ball, to try and keep all these projectiles optimised,
the game uses an object pooling system that stores all the projectiles needed by a specific turret in a list. 
The object pool spawns all it's projectiles when the level loads in, to prevent hitches during gameplay, and manages enabling and disabling them as the turret needs.

The projectiles spawned in by the turrets also have a grabbable object component, 
allowing the player to interact with them, which they can use to their advantage to knock them out the way of the player ball, or even into each other to destroy two at once.
To stop this from being too powerful, the projectiles have a stat that causes the hand to take damage the longer they hold on, forcing them to let go eventually.

## Additional Viewing

[![](https://img.youtube.com/vi/gNS9xRwJfks/0.jpg)](https://youtu.be/gNS9xRwJfks)


