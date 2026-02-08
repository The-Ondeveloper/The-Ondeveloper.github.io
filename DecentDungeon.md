---
layout: default
title: "Decent Dungeon"
permalink: /DecentDungeon
---

# Decent Dungeon

## UI Showcase Video

[![Link to UI showcase](https://img.youtube.com/vi/FUzg1yZIg2g/0.jpg)](https://youtu.be/FUzg1yZIg2g)

## About

Decent Dungeon was a group project made for university, it was a somewhat over-ambitious dungeon crawler -considering the time frame and
team size we had to make it- inspired by the likes of The Elder Scrolls. We came up with the concept through our groups shared fondness
of RPGs, dungeon crawlers, and games like Elder Scrolls.

My role in the group was programming for the UI and character. For the project I developed a fairly simple character with Health and Stamina,
the character contains the inventory component and has the ability to hold equippable items. I also developed the inventory component and the system for creating
inventory items. While I designed and programmed the layout of the UI, it should be clear I did not make the assets for it nor did I create the 3D model for the sword. 

## [Download the game off the repository,](https://github.com/The-Ondeveloper/Process-Pipeline-Repository)

## [or download a build from here.](https://staffsuniversity-my.sharepoint.com/:u:/g/personal/s013512o_student_staffs_ac_uk/IQA7wXJxhjw6Q6V_-Ley0HYpAbbfstPLHZx_9Sd8F7cKLBk?e=gWqfd2)

## Developing the UI

To develop a true dungeon crawler, it is important to have a robust inventory system that can store lots of items and lets the player move them around with ease.
For this project, I went with a minecraft inspired inventory where the player has a permanent tool bar that they can scroll through for easy access to a handful of items
at a time. They can also open their full inventory to manage items using drag and drop. I wanted the UI to be easy to manage, 
so I went with this simple approach of only having two inventories to manage (the toolbar and main inventory) with an intuitive drag & drop system to make
the inventory as easy to weild as possible.

Not many items were developed for the game, but I did set up the system for creating them. All unique data for an item is stored in an Object Type class 
(via UE5's Data Assets), which is also what gets stored in the inventory system, all items in the world are a generic pickup class with their own Object Type. 
Equippable items also store a blueprint which is loaded when the player has the item selected in the toolbar and added to the player's hand.

![The other UI in the game.](Assets/OtherUI.gif)

Alongside the inventory I also developed the other components of the UI, including the health and stamina bars, the pause menu and the start menu.

