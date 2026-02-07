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

## Developing the open world

During development I quickly realised that even when working with small pixel sprites, 
dropping such a shear volume of them into an open world was going to cause performance issues.
To resolve this, I created a system where the world is split into several sub levels which are loaded in and out when the player enters specific loading zones. 
This system not only increased performance at runtime, albeit at the cost of some stuttering when loading between zones,
but also made working on the map a lot easier as Unity was a lot more responsive when working on only one sub-level at a time.

## Boarding the Ship

The core mechanic of the game is being able to board a ship via the ports on each island, it's the most important as you wouldn't be exploring 
many islands without the ability to leave them.
