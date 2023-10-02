---
description: Tutorial to create this PHPMyAdmin search explained in detail
---

# Create Quests

## Quests table structure

![Map Pack capture in game](../.gitbook/assets/a-quests-img0.jpg)

| Name     | Information                                                                | Args                                                                                                        |
| -------- | -------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| assignID | Add a unique number to the quest                                           | (optional, auto-generated)                                                                                  |
| type     | Number of the quest type that will be displayed in the game **\[1]**       | <p><strong>types:</strong><br><code>1</code> = Orbs, <code>2</code> = UserCoins, <code>3</code> = Stars</p> |
| amount   | Amount of orbs/stars/coins to complete the quest **\[2]**                  | A number                                                                                                    |
| reward   | Amount of diamonds that will be rewarded for completing the quest **\[3]** | A number                                                                                                    |
| name     | Name of the quest that will be displayed in the game **\[4]**              | Text                                                                                                        |

## Creating the quest

Learn to access phpMyAdmin: 🔐 [Accessing to phpMyAdmin](site-structure.md)

Learn phpMyAdmin structure: 🔐 [Site Structure](site-structure.md)

<mark style="color:yellow;">⚠ You are required to add a minimum of 3 quests, otherwise the game will not display any quest.</mark>

1. Access to your PHPMyAdmin database and Look for "quests".
2. Open the insert tab.
3. Fill out all fields correctly.
4. Click on "Go".
5. Your quest has been created! ✨

## Trivia

* Previously the quests were configured through the `config/questInfo.php` file along with the chests (currently the file was renamed to dailyChests.php)
* The first quests added by default to the Cvolton core had a name that was not at all appropriate and nothing pleasant for some peoples.
