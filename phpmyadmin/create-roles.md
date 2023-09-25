---
description: >-
  Create a role using PhpMyAdmin and make a good configuration and organization of your gdps roles
---

# Creating a role using PHPMyAdmin

## Role table structure


| Name | Information | Args |
| ---- | ----------- | ---- |
| **RoleID** | Add a unique number to the role | (optional) |
| **priority** | Priority number _(ascending)_ to determine which role is visible in the game and what permissions user will have in the gdps (this is important if multiple roles are assigned to a user) | (Numeric) (No optional) |
| **roleName** | Name that you will give to the role | (optional but it is important if you will have several roles) |
| **commandRate** | Permission to use the !rate command | (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandFeature** | Permission to use the !feature command | (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandEpic** | Permission to use the !epic command | (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandUnepic** | Permission to use the !unepic command | (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandVerifycoins** | Permission to use the !verifycoins command| (Disabled by default) | [0: Disabled / 1: Enabled] |
| **commandDaily** | Permission to use the !daily command| (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandWeekly** | Permission to use the !weekly command| (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandDelete** | Permission to use the !delet command| (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandSetacc** | Permission to use the !setacc command| (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandRenameOwn** | Permission to use the !rename command itself| (Enabled by default) [0: Disabled / 1: Enabled] |
| **commandRenameAll** | Permission to use the !rename command at any level| (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandPassOwn** | Permission to use the !pass command itself| (Enabled by default) [0: Disabled / 1: Enabled] |
| **commandPassAll** | Permission to use the !pass command at any level| (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandDescriptionOwn** | Permission to use the !description command itself| (Enabled by default) [0: Disabled / 1: Enabled] |
| **commandDescriptionAll** | Permission to use the !description command at any level| (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandPublicOwn** | Permission to use the !public command itself| (Enabled by default) [0: Disabled / 1: Enabled] |
| **commandPublicAll** | Permission to use the !public command at any level| (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandUnlistOwn** | Permission to use the !unlist command itself| (Enabled by default) [0: Disabled / 1: Enabled] |
| **commandUnlistAll** | Permission to use the !unlist command at any level| (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandSharecpOwn** | Permission to use the !sharecp command itself| (Enabled by default) [0: Disabled / 1: Enabled] |
| **commandSharecpAll** | Permission to use the !sharecp command at any level| (Disabled by default) [0: Disabled / 1: Enabled] |
| **commandSongOwn** | Permission to use the !song command itself| (Enabled by default) [0: Disabled / 1: Enabled] |
| **commandSongAll** | Permission to use the !song command at any level| (Disabled by default) [0: Disabled / 1: Enabled] |
| **profilecommandDiscord** | Permission to use the !discord command itself| (Enabled by default) [0: Disabled / 1: Enabled] |
| **actionRateDemon** | Permission to set a demon difficult via "Rate demon" button in the game| (Disabled by default) [0: Disabled / 1: Enabled] |
| **actionRateStars** | Permission to rate a level via "Suggest stars" or "Rate stars" button in the game| (Disabled by default) [0: Disabled / 1: Enabled] |
| **actionRateDifficulty** | Permission to set level difficult via "Rate difficult" button in the game| (Disabled by default) [0: Disabled / 1: Enabled] |
| **actionRequestMod** | Permission to obtain moderator permission and moderator buttons via "req" button in the game| (Disabled by default) [0: Disabled / 1: Enabled] |
| **actionSuggestRating** | Permission to create star suggestions| (you can view that in PHPMyAdmin "suggest" table or suggestList.php in tools)| (Disabled by default) [0: Disabled / 1: Enabled] |
| **actionDeleteComment** | Permission to delete comments on users or levels in the game| (Disabled by default) [0: Disabled / 1: Enabled] |
| **toolLeaderboardsban** | Permission to ban/unban user via leaderboardsBan.php/leaderboardsUnban.php in tools| (Disabled by default) [0: Disabled / 1: Enabled] |
| **toolPackcreate** | Permission to create map packs via packCreate.php in tools| (Disabled by default) [0: Disabled / 1: Enabled] |
| **toolQuestsCreate** | Permission to create quests via addQuests.php in tools| (Disabled by default) [0: Disabled / 1: Enabled] |
| **toolModactions** | Permission to display moderator account activity publicly via tools or dashboard| (Disabled by default) [0: Disabled / 1: Enabled] |
<<<<<<< HEAD
| **toolSuggestlist** | Permission to view level suggest via suggestList.php in tools | (Disabled by default) [0: Disabled / 1: Enabled] |
| **dashboardModTools** | Permission currently deprecated | (0 by default)
| **modipCategory** | Place a [category ID](create-modip.md) | (from the "modipperms" table)
| **isDefault** | Determine if the role applies to all players by default| (Disabled by default) [0: Disabled / 1: Enabled] |
| **commentColor** | Place a RGB comment color | (000,000,000 by default) (RGB format)
| **modBadgeLevel** | Place a badge level | (None by default) [0: None / 1:Moderator / 2: Elder Moderator / Any number] |
=======
| **toolSuggestlist** | Permission to view level suggest via suggestList.php in tools| (Disabled by default) [0: Disabled / 1: Enabled] |
| **dashboardModTools** | Permission currently deprecated| (0 by default)
| **modipCategory** | Place a category ID| (from the "modipperms" table)
| **isDefault** | Determine if the role applies to all players by default| (Disabled by default) [0: Disabled / 1: Enabled] |
| **commentColor** | Place a RGB comment color| (000,000,000 by default) (RGB format)
| **modBadgeLevel** | Place a badge level| (None by default) [0: None / 1:Moderator / 2: Elder Moderator / Any number] |
>>>>>>> 90e47eb281e7431195384a940e76fac127fdc521

## Creating a role

1. Open phpMyAdmin & login.
2. Select the database starting with "gdps_".
3. Look for "roles".
4. Open the insert tab.
5. Fill out all fields correctly.
6. Click on "Go".
7. You have created your role correctly!
