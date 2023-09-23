---
description: You can use commands on a level to change how the level is presented.
---

# Level Commands

These commands can be used on a level in the comments section.\
You should get a false error when posting those, which _usually_ means that using the command worked.

**More information about command permissions:** 🔐 [Create Roles](../phpmyadmin/create-roles.md)

***

| Command | Description | Args | Permission |
| ------- | ----------- | ---- | ---------- |
| **!rate** (Difficulty) (Amount of Stars) (Verify Coins) (Set Featured) | Rate a level | **Difficulty:**<br>Auto, Easy, Normal, Hard, Harder, Insane, Demon _(If the difficulty does not exist, it will put NA by default)_<br>**Amount of stars:** In the amount of stars you can place a personalized amount.<br>**Verify coins:** You can also enter if the coins are collectable [ 1 = Verified _(Silver coins)_, 0 = Not verified _(Bronze Coins)_ ] <br>**Set Featured:** You can set the level is featured or not: [ 1 = Featured, 0 = Not Featured ] | commandRate |
| **!feature** | Set featured a level |  | CommandFeature |
| **!epic** | Set epic a level | | CommandEpic |
| **!unepic** | Remove epic a level | | CommandUnepic |
| **!setacc** (Account Name) | Move a level to a specific account | **Account Name:** Name of the account who will now own the level | CommandSetacc |
| **!verifycoins** (Mode) |  Set if coins of the level are collectable | **Mode:** 1 = Verified (Silver coins), 0 = Not verified (Bronze Coins) | CommandVerifycoins |
| **!daily** | Queues the level as a daily level.  | | CommandDaily |
| **!weekly** | Queues the level as a Weekly level. | | CommandWeekly |
| **!delet** | Delete a level from the GDPS Server. | | CommandDelet |
| **!pass** (Password) | Update the level password | **Password:** Numbers only, 4-6 digits (Set password to 0 make it a free-copy) | CommandPassOwn / CommandPassAll |
| **!description** (Description) | Update the level description | **Description:** 300 characters limit. (Special Characters are removed for safety) | CommandDescription |
| **!public** | Set a level publicly visible | | CommandPublicOwn / CommandPublicAll |
| **!unlist** | Set a level only viewable via Level ID | | CommandUnlistOwn / CommandUnlistAll |
| **!sharecp** (username) |  Share Creator Points with another user (CP will be split equally) | **username:** Name of the account who will distribute the creator points (max: 1 person) | CommandSharecpOwn / CommandSharecpAll |
| **!ldm** | Force LDM button in a level | | |
| **!unldm** | Force LDM button disabled in a level | | |
| **!rename** (level name) | Change the level name | **level name:** 300 characters limit. (Special Characters is removed) | CommandRenameOwn / CommandRenameAll |
| **!song** (SongID) | Change the song of the level | **SongID:** Numbers only, Newgrounds songs and song reuploaded are supported | CommandSongOwn / CommandSongAll |


