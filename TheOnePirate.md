---
layout: default
title: The One Pirate
permalink /TheOnePirate
---

# The One Pirate

## Full Playthrough Video

[![Link to Full playthrough video](https://img.youtube.com/vi/3jNirX8R5xU/0.jpg)](https://youtu.be/3jNirX8R5xU)

## About

The One Pirate is a game made in Unity for a university module about C# and game engine development.
In it, you are are a pirate who must explore an open-world ocean, collect treasure, and find the great **Legendary Treasure**
hidden on a mysterious island somewhere. The pirate can roll to traverse islands and evade enemies, shoot to fight back against them, and of course,
board his ship to traverse the ocean.

## [Download the game off the repository,](https://github.com/The-Ondeveloper/TopDownFramework)

## [or download a build from here.](https://staffsuniversity-my.sharepoint.com/:u:/g/personal/s013512o_student_staffs_ac_uk/IQAhZxNFydyRTJwKn5SMJnjWAQP3UYrn6dsccXe-5JMq_c8?e=3Ib3fr)

## Developing the open world

During development I quickly realised that even when working with small pixel sprites, 
dropping such a shear volume of them into an open world was going to cause performance issues.
To resolve this, I created a system where the world is split into several sub levels which are loaded in and out when the player enters specific loading zones, 
their is also a level which is persistently loaded in that contains the player characters, UI, etc. 
This system not only increased performance at runtime, albeit at the cost of some stuttering when loading between zones,
but also made working on the map a lot easier as Unity was a lot more responsive when working on only one sub-level at a time.

## Boarding the Ship

![The start of the game](Assets/TOPGameplay.gif)

The core mechanic of the game is being able to board a ship via the ports on each island, it's the most important as you wouldn't be exploring 
many islands without the ability to leave them. The Pirate and the Ship are really just two seperate player characters on different collision planes.
The various ports across the map access a character manager that keeps track of which character is currently enabled, swapping them out when one overlaps with a port.
The ports also contain entrance exit points the characters teleport to when they are re-enabled.
The Pirate's health bar is always visible, but the ships health bar is hidden when it's left at a port, 
which was a descision made to reduce the amount of unneccessary information on the player's screen.

## Developing the player character

The Pirate has two major abilities, the roll and the projectile he is able to fire. The roll is useful both for evading enemies and for traversing gaps across islands.
While the Pirate is unable to swim and will be kicked back to land if he rolls into the ocean, he can use the roll to 'jump' over small bodies of water,
making it easier to traverse various islands across the map. The ship also has the ability to 'roll' which really just allows it to quickly dash in one direction,
you cannot beach the ship in this game. The Pirates other ability to shoot a small projectile allows it to fight back against enemies, 
the ship lacks this ability, which forces you to play more evasively when out in the ocean.

## Additional Viewing

### Eary Test Gameplay

[![Link to early test gameplay video](https://img.youtube.com/vi/X669oTHtFJE/0.jpg)](https://youtu.be/X669oTHtFJE)

## Credits

### *[RPG Beach Tileset by Stealthix](https://stealthix.itch.io/rpg-beach-tileset)*
