---
description: >-
  Guide to creating your own map packs for your GDPS using PHPMyAdmin explained in detail
---

# Create map packs using PHPMyAdmin

## Mappacks table structure

<img src="../.gitbook/assets/a-mappacks-img0.jpg" width="50%" alt="Map Pack capture in game" />

| Name | Information | Args |
| ---- | ----------- | ---- |
| ID | Add a unique number to the map pack | (optional) |
| name | name of the map pack that will be displayed in the game **[1]** | (no optional) |
| levels | Map pack level IDs separated by commas, example: `15908,981172,39223` | You need 3 level IDs (no optional) |
| stars | Number of stars that the player will get when completing the map pack **[2]** | Minimum: 2 star, Maximum: 10 stars (no optional) |
| coins | Number of star coins that the player will get when completing the map pack **[3]**| Minimum: 1 coin, Maximum: 2 coins (no optional) | 
| difficulty | Map pack difficulty number that will be displayed in the game **[4]** | **Difficulty number list:**<br> `0` = Auto, `1` = Easy, `2` = Normal, `3` = Normal, `4` = Harder, `5` = Insane, `6` = Hard Demon, `7` = Easy demon, `8` = Medium demon, `9` = Insane Demon, `10` = Extreme Demon (no optional) | 
| rgbcolors | Name color of the map pack name that will be displayed in the game **[1]** | RGB Format (no optional) |
| colors2 | Bar color of the map pack name that will be displayed in the game **[5]** | RGB Format (no optional) |




## Creating a map pack

Learn to access PHPMyAdmin: 🔐 [Accessing to phpMyAdmin](site-structure.md)

Learn PHPMyAdmin structure: 🔐 [Site Structure](site-structure.md)



1. Access to your PHPMyAdmin database and Look for "mappacks".
2. Open the insert tab.
3. Fill out all fields correctly.
4. Click on "Go".
5. NICE! You has been created a map pack in your GDPS!

## Trivia

- For a strange reason Cvolton did not separate the level IDs in 3 more columns (contrary to gauntlets).
- Difficulty numbers 6 through 10 do not exist before GD 2.1 version.