---
layout: default
title: Top Down Turret
permalink: /TopDownTurret
---

# Top Down Turret

## Full Playthrough

[![Full playthrough video.](https://img.youtube.com/vi/SNdaokZKR_M/0.jpg)](https://youtu.be/SNdaokZKR_M)

## About

Top Down Turret is a university project made in a supplied framework. The goal of the project was to expand on the framework by creating
original weapons and mechanics, as well as a fleshed out level to use them in. The concept behind my project was to add RPG mechanics to the game,
including an EXP system and upgrade system with branching upgrades for each weapon. 

## [Download the game off the repository,](https://github.com/The-Ondeveloper/Mechaniscs-Prototyping)

## [or download a build from here.](https://staffsuniversity-my.sharepoint.com/:u:/g/personal/s013512o_student_staffs_ac_uk/IQCuShF8dW71Sa8ZILTXe_U4AUNm11UyRf2lKFqSIsMxY9Q?e=PBPQPQ)

## Developing the RPG mechanics

Every time the player gets enough EXP to level up, they are given the option to upgrade one of their currently equipped weapons. 
Each weapon can be upgraded once and each level up has two options that would lead to branching paths if more levels were to be added. 
To make this upgrade system feasible, I reworked the framework to convert all weapons into Data Assets
and simplified the weapons to be a single class that defines its functionality using its current Data Asset. The Data Asset contains data such as what projectile to fire
-which I also converted to use Data Assets- the projectile spread, fire rate, secondary fire (if any) what weapons the weapon can upgrade into, and etc. 
This means rather than upgrades being something that gets attached onto a base weapon, 
they are just another weapon in their own right that a weaker weapon can be upgraded into.

## Developing the weapon variety

The weapon and projectiles are both represented by a single base class that uses Data Assets to determine its unique logic.
The weapon data assets contain fields like primary and secondary projectile to fire, fire rate, projectile spread, and what weapons it can be upgraded into.
Meanwhile, the projectile data assets contians fields like damage, life span, gravity, projectile speed, etc. 
With these tools in place, I was able to develop the weapons and projectiles at a rapid pace; in the final project their are 6 base weapons, 
with two upgrades each for a total of 18 weapons, and including secondary fires there are around 13 projectile types.
These weapons include a generic starter weapon, a shotgun, an smg, a sniper, a boomerang shot, and a grenade launcher.

![Choosing an upgrade in Top Down Turret](Assets/TDTGameplay.gif)

The weapon class can store up to three weapon data assets, which acts as an inventory in-game, 
when the player has multiple weapons equipped they can freely swap between them and if they pick up a new weapon when their inventory is already full,
it swaps their currently equipped weapon out from the new one. The old weapon becomes a pick up that gets dropped on the ground, allowing the player to manage their
inventory and choose a loadout of their preferred weapon, without the need for an inventory menu.

## Developing the enemy variety

The game features a number of enemy types, categorised first by their AI behaviour and then by what weapon they use.
All the weapons used by enemies are weapons that can also be unlocked by the player, such as the shotgun, smg and grenade launcher.
The AI types featured in the game include enemies that chase the player, enemies that move randomly, and enemies that patrol a set path.
The final boss of the game features a phase mechanic, every few seconds he'll swap between different behaviours seen by individual enemies
throughout the game, these phase changes also affect what weapons he can use to attack you, making the boss fight somewhat of a bullet hell.

## Designing the level

I ended up designing quite a lengthy level for this project as I wanted to give players a chance to level up multiple times through fighting enemies.
I also followed a design philosophy of slowly introducing more mechanics as the game goes on, 
I wanted a section dedicated to tackling each enemy type and finding each new weapon to give players a chance to experiment with all the mechanics at a decent pace,
which also contributed to developing quite a long level.
I tried to keep the level design fresh in each section with branching paths, hidden areas and frequent changes in scenery and lighting. 