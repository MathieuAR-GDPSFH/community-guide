---
description: >-
  There isn't really a tools page to help you create a gauntlet,
  so this will guide you through creating a gauntlet via phpMyAdmin.
---

# Create gauntlets using phpMyAdmin

## Gauntlets ID list

In version 2.11 there are a total of **15 gauntlets** but through a RobTop live via Twitch showed [30 new gauntlets](https://youtu.be/HWMdI-7Myns) (subject to changes) that will be released in 2.2 version.

These 2.2 gauntlets are **partially implemented** in [Geometry Dash Subzero](https://play.google.com/store/apps/details?id=com.robtopx.geometrydashsubzero) and their textures can be found.

| Gauntlet ID | Gauntlet name | Game Version |
| -- | ------------- | ------------ |
| 1| Fire| 2.1 |
| 2| Ice| 2.1 |
| 3| Poison| 2.1 |
| 4| Shadow| 2.1 |
| 5| Lava| 2.1 |
| 6| Bonus| 2.1 |
| 7| Chaos| 2.1 | 
| 8| Demon| 2.1 | 
| 9| Time| 2.11 |
| 10| Crystal| 2.11 |
| 11| Magic| 2.11 |
| 12| spike| 2.11 |
| 13| Monster| 2.11 |
| 14| Doom| 2.11 |
| 15| Death| 2.11 |
| 16| Forest| 2.2 |
| 17| Rune| 2.2 |
| 18| Force| 2.2 |
| 19| Spooky| 2.2 |
| 20| Dragon| 2.2 |
| 21| Water| 2.2 |
| 22| Haunted| 2.2 |
| 23| Acid| 2.2 |
| 24| Witch| 2.2 |
| 25| Power| 2.2 |
| 26| Potion| 2.2 |
| 27| Snake| 2.2 |
| 28| Toxic| 2.2 |
| 29| Halloween| 2.2 |
| 30| Treasure| 2.2 |
| 31| Ghost| 2.2 |
| 32| Spider| 2.2 |
| 33| Gem| 2.2 |
| 34| Inferno| 2.2 |
| 35| Portal| 2.2 |
| 36| Strange| 2.2 |
| 37| Fantasy| 2.2 |
| 38| Christmas| 2.2 |
| 39| Surprise| 2.2 |
| 40| Mystery| 2.2 |
| 41| Cursed| 2.2 |
| 42| Cyborg| 2.2 |
| 43| Castle| 2.2 |
| 44| Grave| 2.2 |
| 45| Temple| 2.2 |

## Gauntlet table structure

| Name | Information | Args |
| ---- | ----------- | ---- |
| ID | ID number of the gauntlet that will appear in the game (table previously shown) | (no optional) |
| level1 | ID of the level that will appear in the gauntlet | (no optional) |
| level2 | ID of the level that will appear in the gauntlet | (no optional) |
| level3 | ID of the level that will appear in the gauntlet | (no optional) |
| level4 | ID of the level that will appear in the gauntlet | (no optional) |
| level5 | ID of the level that will appear in the gauntlet | (no optional) |

⚠ **Note: Gauntlet levels are organized by difficulties _(easiest to hardest)_, ignoring the order you place in the table.**

## Creating gauntlet

Learn to access PHPMyAdmin: 🔐 [Accessing to phpMyAdmin](site-structure.md)

Learn PHPMyAdmin structure: 🔐 [Site Structure](site-structure.md)

1. Access to your PHPMyAdmin database and look the table "gauntlets"
2. Open the insert tab
3. Fill out all fields correctly.
4. Click on "Go"
5. Congratulations, you have created a gauntlet using PHPMyAdmin! 🔥

**Have you not understood?** Watch this video tutorial (Credits to Matto58)

{% embed url="https://www.youtube.com/watch?v=iISmYc0F7es" %}

## Trivia

- The only gauntlet without capitalisation in-game is the 'spike' Gauntlet.
- Gauntlets work like map packs but with fewer functions.