---
description: A very lengthy, but in-depth explanation of the PhpMyAdmin tables
---

# In-depth explanation of PhpMyAdmin tables and columns

Tables: Tables in PhpMyAdmin have columns and indexes.\
An example of a table is the accounts table.

Columns: Columns are columns in PhpMyAdmin tables that make the tables function for the server.\
An example of a column is accountID in the accounts table.

## Access the PhpMyAdmin tables
    
If you are confused on how to access all the tables, heres how:
First, after logging in, click the "+" on the side next to gdps_(gdpsname).
To access the tables, click the text of the name of the tables.
(On phone, enable desktop site for PhpMyAdmin to work properly.)

### Acccomments: This table displays all the account comments players have made on their profiles.

* userID: Tells you what user ID made the comment.
* Comment: Displays the content of the account comment. (it is encrypted though)
* Secret: Unused
* CommentID: Unique ID of the account comment.
* Timestamp: The unix timestamp. (basically when the comment was uploaded. You can use an online calculator to see the actual date and time.)
* Likes: displays how many likes it has. (A negative likes amount means dislikes.)
* isSpam: Shows if the comment has enough dislikes to be marked as spam

### Accounts: This table displays all the accounts in the GDPS.

* userName: Tells you the account's username it was registered with.
* password: Gives you password hash for the password of their account. (You can't decrypt this information, you can only use a website to check if the hash corresponds to text you type.)
* gjp2: Encrypted password hash
* email: Displays the email the account was registered with.
* accountID: Unique ID of the account. (useful when something in PhpMyAdmin asks for accountID.)
* isAdmin: This adds all permissions to your GDPS account.
* mS: This is the message state of the account. It doesn't appear to work though.
* frS: This is the friend request state of the account. It doesn't appear to work though.
* cS: This is the comment state(who to show your comment history to). It doesn't appear to work though.
* youtubeurl: The YouTube account URL the user has linked to their profile. (It only shows you what you put after the / in youtube.com/. Example: youtube.com/GoogleDrive.)
* twitter: The Twitter(X) account URL the user has linked to their profile. (Again it only shows you what to put after the / in twitter.com URL. Example: twitter.com/discord.)
* twitch: The Twitch account the user has linked to their profile. (This only tells you what to put after the / in twitch.tv URL. Example: twitch.tv/epicgamer.)
* salt: It is not used in a GDPS.
* registerDate: Tells you what date the user registered their account in unix timestamp format. (Use a online calculator to find the actual date the account was registered on.)
* friendsCount: Displays the amount of friends the user has added on their account.
* discordID: I think this was used for the discontinued Cvolton GDPS bot.
* discordLinkRequest: Also used for discontinued Cvolton GDPS bot.
* isActive: Will either be 0 or 1. 0 means the account is not activated while 1 means the account is activated.

### Actions: This table will display automatic server-side actions.

* ID: This is the unique ID of the action.
* type: This tells you the type of action that was issued. (2 = A succesful login into a account; 6 = When a user fails to login to their account. It can also be 6 because the user's account is disabled from failing to login 6 times; 8 = When a level gets deleted off the servers; 9 = When a user updates their stats in-game; 16 = This is used for GJP verification every hour. It will only appear if sessionGrants is set to true in `config/security.php`)
* value: This tells you what value was changed to what. (2 = The account ID of the user who logged in successfully; 6 = account ID that was either disabled or that the user failed to login to; 8 = the ID of the level that was deleted; 9 = the amount of stars the user collected; 16 = account ID that was verified.)
* timestamp: the unix timestamp of when the action happened. ( You can use an online calculator to tell you when it was exactly.)
* value2: Similar to the values column, this column just displays different information. (2 = This displays the IP of the user who successfully logged in; 6 = This displays the IP of the user who failed to login/account disabled; 8 = This displays the IP of the user who deleted the level; 9 = This displays the amount of secret coins the user collected; 16 = This displays the IP of the user who has been verified.)
* value3: Similar to the other value columns, just for one type of action. (9 = This displays the amount of demons the user completed.)
* value4: Similar to the other value columns, also for one type of action. (9 = This displays the amount of user coins the user collected.)
* value5: Similar to the other value columns, also for one type of action. (9 = This displays the amount of diamonds the user collected.)
* value6: This is for a 2.2 item. (9 = This will display the amount of moons the user has collected.)
*   account: This is for action type 9. This displays the user ID of the user who changed their stats.

    (Note: When I put numbers such as "2 =" I was referring to the action type number 2.) (Other Note: There is already a guide about this but I only put this in here because it is to do with PhpMyAdmin.)

### Actions\_downloads: This table lists every level download. It doesn't count another download when a user downloads a level again.

* id: This is the unique ID for the download of the level.
* levelID: This tells you what level ID was downloaded.
* ip: This tells you the IP of the user who downloaded the level. It is in varbinary(4) format.
* uploadDate: Displays the date and time the level was downloaded in a normal format. (Year-Day-Month-Hours-Minutes-Seconds.)

### Actions\_likes: This table lists every level a user has liked.

* id: This is the unique ID for the like on a level.
* itemID: This is the level ID that was liked.
* type: the type of like. 1 = level, 2 = comment on a level and 3 = account comment.
* isLike: Tells you whether it was a like or a dislike. 0 = dislike and 1 = like.
* ip: This is the IP of the user who liked the level. It is in varbinary(4) format.
* uploadDate: The date and time of when the level was liked. It is displayed in normal format. Year-Day-Month-Hours-Minutes-Seconds.

### Bannedips: this table displays what IP addresses are leaderboard banned.

* ID: The unique ban ID.
* IP: The IP you want to leaderboard ban.

### Blocks: This table lists any users who have blocked each other

* ID: The unique ID of the block.
* person1: the Account ID of the user who clicked "block" button.
* person2: the Account ID of the user who "person1" blocked.

### Comments: This table lists comments on levels.

* userID: The ID of the user who commented.
* userName: The username of the user ID who commented on the level.
* Comment: This displays the content of the uploaded comment. (It is base64 encoded and you can decode it to see the content too.)
* Secret: None
* levelID: The ID of the level that the comment was made on.
* commentID: Unique ID of a comment.
* timestamp: The unix timestamp of when the comment was uploaded. (You can use an online converter to get the actual date.)
* likes: The amount of likes on the comment.
* percent: The percent the user got on the level when they uploaded the comment.
* isSpam: This will only be 1 if the comment has a lot of dislikes. (0 is not spam and 1 is spam.)

### Cpshares: This is the table that lists all the levels !sharecp command was used on.

* shareID: This is the unique ID of the Creator Points share.
* levelID: the ID of the level you used !sharecp on.
* userID: The ID of the user you shared the Creator Points with.

### Dailyfeatures: This table lists all the daily and weekly levels.

* feaID: The unique ID of the daily/weekly level.
* levelID: The ID of the level that is daily/weekly.
* timestamp: This is the unix timestamp of when the level was made daily/weekly. (You can use an online converter to get an actual date.)
* type: The type. It can only be daily or weekly. 0 is daily and 1 is weekly. (In 2.2, type 2 is the event level.(Added in latest GD 2.2 Subzero)

### Friendreqs: This table lists all the friend requests that have been sent.

* accountID: The ID of the account that sent the friend request.
* toAccountID: The ID of the account that the friend request was sent to.
* comment: This displays the message that someone sent with the friend request. (It might be blank for some friend requests sent because the user didn't attach a message with it.)
* uploadDate: The unix timestamp of when the friend request was sent. (You can use an online converter to see the actual date.)
* ID: The unique ID of the friend request.
* isNew: It will be either 0 or 1. 0 meaning the user sent a friend request before and 1 being the user hasn't sent a friend request before.

### Friendships: This table lists all the users who have added each other as friends.

* ID: The unique ID of the friendship.
* person1: The account ID of the person who accepted the friend request
* person2: The account ID of the person who sent the friend request.
* isNew1: It will be 0 or 1. 0 meaning it is not new and the user has added the other person as a friend before and 1 meaning it is new. (This is for person 1 too.)
* isNew2: The same as isNew1, just for person 2.

### Gauntlets: This table lists the gauntlets and allows you to make gauntlets.

* ID: The ID of the guantlets. (1 = fire, 2 = fire, 3 = poison, etc.) It follows real Geometry Dash's order of gauntlets.
* level1: The first level.
* level2: The second level.
* level3: The third level.
* level4: The fourth level.
* level5: The Fifth level.

    (Note: The levels will be ordered by difficulty so if you put a 4 star as level1 and a 2 star as level2, level 1 will be the 2 star.)

### Levels: This table lists all the uploaded levels in the GDPS.

* gameVersion: This is the version of the game the level was made and uploaded in. (21 means version 2.1, 20 would mean version 2.0 and so on.)
* binaryVersion: This is supposed to be the update version not the game version. Although it does not display properly.
* userName: This is the username of the creator of the level.
* levelID: This is the unique ID of the level.
* levelName: This displays what the level is called in-game.
* levelDesc: This displays the contents of the level description is. (It is base64 encoded and you can decode it.)
* levelVersion: The version of the level.
* levelLength: The length of the level. (0 = Tiny; 1 = Short; 2 = Medium; 3 = Long; 4 = XL; 5 = Plat.)
* audioTrack: This tells you the ID of the music, if it is a default song used.
* auto: This will mean the level is rated auto if it is 1. 0 means it is not rated auto.
* password: The level copy password. (If there is no password it will be 0.)
* original: This will either be 0 or the ID of the original level that it was copied from.
* twoPlayer: This displays either 0 or 1. 0 being the level is not 2 player and 1 being the level is 2 player.
* songID: This displays the ID of the custom song used.
* songIDs: this tells you the IDs of the songs used in the level if multiple were used.
* sfxIDs: this tells you the IDs of the sfx used in the level.
* objects: This displays the amount of objects the level has.
* coins: This displays how many coins the level has. (It ranges from 0 - 3)
* requestedStars: The amount of stars requested when the level was uploaded.
* extraString: This is a complicated topic to explain here but put simply, it is other objects and layers of objects and much more. Here is a link to [the detailed explanation](https://github.com/Wyliemaster/gddocs/blob/master/docs/resources/client/level-components/capacity-string.md).
* levelString: This is empty as I don't think it is used. (I will update this if it is used or was used.)
* levelInfo: This displays the level's code. (If you look in CCLocalLevels.dat file, level code will look like this too.)
* secret: This is used to identify if you are using a Geometry Dash client to upload levels or if you are using an external client. For more information about secrets [check out this documentation.](https://github.com/Wyliemaster/gddocs/blob/master/docs/reference/secrets.md)
* starDifficulty: This displays what difficulty the level is. (0 = N/A; 10 = Easy; 20 = Normal; 30 = Hard; 40 = Harder; 50 = Insane; 50 = Auto; 50 = Demon;)
* downloads: This displays the amount of downloads the level has.
* likes: This displays how many likes the level has.
* starDemon: This is used to identify if the level is a demon or not. 0 = not demon and 1 = demon.
* starAuto: This is used to identify if the level is star auto rated or not. 0 = not auto 1 is auto.
* starStars: This is used to display how many stars the level is rated. (Example: 10)
* uploadDate: This is the date the level was uploaded in unix timestamp form. (You can use an online converter to get the exact date.)
* updateDate: This is the date the level was updated in unix timestamp form0. (You can use an online converter to get the exact date.) If the level was never updated then this will be the upload date.
* rateDate: The date the level was rated in unix timestamp form. (You can use an online converter to get the exact date.) It will be either the star or no star rate date.
*   starCoins: This tells you if the coins are verified or not. (0 = not verified coins; 1 = verified coins.)

    <mark style="color:red;">**DO NOT SET starCoins TO 2 OR HIGHER AS IT WILL BREAK YOUR LEVELS TAB!**</mark>
* starFeatured: This indetifies whether the level is featured or not. (0 = not featured; 1 = featured.)
* starHall: This identifies whether the level goes into the "Hall of Fame" tab or not. 0 = Not in Hall of Fame; 1 = In Hall of Fame.
* starEpic: This identifies whether the level is epic rated or not. (0 = Not epic rated; 1 = The level is epic rated; 2 = The level is legendary rated in 2.2; 3 = mythic/godlike rating on the level in 2.2 as well)
* starDemonDiff: This tells you what demon difficulty the level is rated. (0 = Non-demon rated levels; 1 = Easy demon; 2 = Medium Demon; 3 = Hard Demon; 4 = Insane Demon; 5 = Extreme Demon.)
* userID: The ID of the user who uploaded the level.
* extID: The account ID of the user who uploaded the level.
* unlisted: This tells you whether the level is unlisted or not. (0 = public; 1 = unlisted.)
* originalReupload: Only displays a level ID of the original level if you re-uploaded a level from another GDPS using reupload.php. (It will be the GDPS you re-uploaded the level from, original level ID)
* hostname: The IP address of the level uploader.
* isCpShared: This identifies whether the !sharecp command was used on the level.
* isDeleted: This identifies whether the level is deleted from the servers but is still in the database. (0 = not deleted; 1 = deleted.)
* isLDM: This identifies whether the level has an LDM button or not. (0 = No LDM button; 1 = LDM button.)
* unlisted2: Tells you if the level is unlisted and availible for public as long as users have the ID. (I think I'm not 100% sure yet.)
* wt: I am not sure (I will find out and update this.)
* wt2: also not sure.
* ts: Not sure
* settingsString: Unused.

### Levelscores: This table lists the percentages players have got on levels.

* scoreID: This is a unique ID to each score.
* accountID: The ID of the account that got the score.
* levelID: The ID of the level the user got the score on.
* percent: The percentage the user got on the level.
* uploadDate: The date in which the user got the score in unix timestamp format. (You can use an online converter to find the exact date.)
* attempts: The amount of attempts the user took to get the percentage on the level.
* coins: The amount of coins collected (if applicable). (Ranges from 0 - 3.)
* clicks: The amount of times the user clicked when they got the percent on the level.
* time: The amount of time it took for the user to get the percentage on the level.
* progresses: The percentages achieved before the user's highest percentage on the level.
* dailyID: The daily ID of the daily level they got a percentage on. (Only applicable if the user actually got a percentage on a daily level.)

### Links: This tables displays any servers you have used linkaccount.php with

* ID: The unique ID of the link
* accountID: Your GDPS account ID.
* targetAccountID: The account ID on the server you linked your account to.
* server: The server you linked your account to.
* timestamp: The date you linked the account in unix timestamp format. (You can use an online converter to get the exact date.)
* userID: The ID of your GDPS user.
* targetUserID: The ID of your user in the other server. (**Note: linkaccount.php only works between other GDPS's**)

### Lists: This table lists all the level lists created in the GDPS
* listID: The unique ID of the list.
* listname: The name of the list.
* listDesc: The description of the list (it i encoded in base64, you can decode base64 by going to https://base64decode.org/)
* listVersion: The version of the list (just like level version)
* accountID: The ID of the account who uploaded the list.
* downloads: The amount of downloads the list has
* starDifficulty: the difficulty of the list. (0 = auto; 1 = easy; 2 = normal; 3 = hard; 4 = harder; 5 = insane; 6 = easy demon; 7 = medium demon; 8 = hard demon; 9 = insane demon; 10 = extreme demon. any value above 10 is just NA)
* likes: The amount of likes the list has
* starFeatured: This tells you if the list is featured or not. (0 = not featured; 1 = featured.)
* starStars: This tells you how many diamonds the list gives you when you complete it.
* listlevels: this tells you the IDs of the levels in the list.
* uploadDate: This tells you the date the level was uploaded. (it is in unix timestamp format so using an online converter will tell you the actual date in regular form)
* updateDate: This tells your the date the level was updated on (if it was) It is also in unix timestamp format so you can use an online converter to get the date in regular form.
* original: This tells you the ID of the list that the current list was copied from (if it was copied)
* unlisted: This tells you if the list is unlisted or listed. (0 = listed aka public;  = unlisted)

### Mappacks: This table lists the map packs that are created in the GDPS and allows you to create Map packs.

* ID: The unique ID of the map pack.
* name: The name of the map pack.
* levels: The ID's of the levels in the map pack.
* stars: The amount of stars the map pack will give.
* coins: The amount of secret coins the map pack will give.
* difficulty: The difficulty face that will show up on the map pack in-game. (0 = auto; 1 = Easy; 2 = Normal; 3 = Hard; 4 = Harder; 5 = Insane; 6 = Demon.)

### Messages: This table displays all the messages sent to other users from other users.

* userID: The ID of the user sending the message.
* userName: The username of the user sending the message.
* body: The body of the message sent. (It is base64 encoded, you can decode this text though.)
* subject: The subject of the sent messages. (Also base64 encoded.)
* accID: The ID of the account sending the message.
* messageID: The unique ID of the message.
* toAccountID: This tells you the account ID the message was sent to.
* timestamp: This tells you when the message was sent in unix timestamp format. (You can use an online converter to see the exact date.)
* secret: Read [this documentation for more information.](https://github.com/Wyliemaster/gddocs/blob/master/docs/reference/secrets.md)
* isNew: This displays whether the message is new and that the user hasn't sent a message to the user before. (0 = sent message before; 1 = never sent message before.)

### Modactions: This table lists all the actions done by moderators in-game.

* ID: Unique ID for all moderator actions.
* type: this has many different types, whether it is from rating a level to deleting a level. (1 = rating a level a demon, or any other difficulty using !rate command; 2 = featuring a level; 3 = When you verify coins; 4 = rating a level non-demon; 5 = unsure; 6 = Using !delete on a level; 7 = using !setacc on a level; 8 = using !rename on a level; 9 = Not sure for now; 10 = using demon moderator rate button; 11 = creating a map pack from tools page; 15 = I am unsure currently; 16 = using !song command on a level and changing it's song ID; 25 = creating a quest. I think that is all the types, well the ones I know about for now. I will update this when I get all the information.)
*   Value: this depends on the action but if you look at certain actions it will display the following:

    1: Rating a level demon or other difficulties using !rate command displays: \[Difficulty].

    2: Featuring a level will display 1 or 0 (depending on what you typed with !feature, if you just typed "!feature", it'll make it 1, if you type "!feature 0" it will display 0 and also un-feature the level.)

    3: Verifying the coins of a level will display 1 under values column.

    4: This will display a 1 when you do !epic and it will display a 0 if you do !unepic.

    5: It is now removed from mod\_actions table and moved to actions\_likes as type 2.

    6: It will display a 1 if you used !delete on a level.

    7: It will display the username of the account you set a level to using !setacc command.

    8: It will display the new name of the level after using !rename on an level.

    9: unsure

    10: It will display Easy,Medium,Hard,Insane or Extreme here depending on the demon difficulty you set it to using the demon rate moderator button.

    11: It will display the name of the map pack here if you used packcreate.php for a map pack from tools page.

    15: unsure

    16: It will display the new song ID of the level you used the !song command on a level.

    25: it will display the ID of what you need to get for a quest. (later on you will see the ID's of orbs, diamonds and stars for the quests table.)
* timestamp: This displays the date and time the action was issued on in unix timestamp format. (You can use an online converter to get exact date.)
* value2: This displays other values, it can display the amount of orbs,diamonds or stars required for a quest, the level ID's that are in a map pack and more.
* value3: This column will display a level ID if the action was executed on a level, it displays the amount of stars a map pack will reward you with when you complete the map pack.
* value4: This column can display the amount of secret coins and map pack will reward you with when it is completed and it displays a 1 when moderator action type 5 is executed.
* value5: I have no idea what moderator action will add a value to this column.
* value6: Another column that I am unsure of what will be displayed here.
* account: The ID of the account that executed the action.
* value7: This column displays the RGB colour code for a map pack's text.

### Modipperms: This table is for creating special permissions for a role. (I am not 100% sure what the special permissions are.)

* categoryID: The unique ID of the category.
* actionFreeCopy: This identifies whether your role can copy any level. Copy any level like copy hack. (0 = no permissions to copy all levels; 1 = permissions to copy all levels.)

### Modips: This table lists all the IP's of moderators and the moderators who have modipperms.

* ID: This is a unique ID of the IP address of the moderator.
* IP: This column displays the moderator's IP address.
* accountID: The ID of the moderator's account.
* modIPCategory: This will be the ID of the modipperms category you set. (If you made a role that has modIPPerms and the value is set to the ID of the category, it will appear under the modips table.)

### Platscores: This table tells you all the leaderboard scores on platformer levels in the GDPS.
* ID: The ID of the account who got the score.
* levelID: The ID of the level the score was on
* time: The time it took for the user to complete the level.
* points: The points the user got on that level.
* timestamp: The date the user got the score on (it is in unix timestamp format so you can use an online converter to get the actual date in regular format)
### Quests: This table lists all the created quests in the GDPS and allows you to make quests.

* ID: The unique ID of the quest.
* type: The type of in-game item you need to collect. (1 = orbs; 2 = user coins; 3 = stars.)
* amount: The amount of (type) the user needs to collect to complete the quest.
* reward: This is the amount of diamonds you will receive for completing the quest.
* name: The name of the quest.

(Note: You will need a minimum of 3 quests for the quests to work in-game.)

### Reports: This table lists any level's that a user has reported.

* ID: The unique ID of the report.
* levelID: The ID of the level the user reported.
* hostname: The IP of the user who reported the level.

### Roleassign: This table displays all the users who have a role added to them. You can also assign a role to a user here.

* assignID: The unique ID of the role assign.
* roleID: the ID of the role you want to assign.
* accountID: The ID of the account you want to assign to a user.

### Roles: This is the table that lists all the roles and this table allows you to create roles.

* roleID: The unique ID of the role.
* priority: This works like this: If you have a role that has a priority of 2 assigned to your user and you have a role with a priority of 1 assigned to your user, the role with the higher priority number will be the role that shows up on your profile. It will also be the role that you have permissions from. (The other role with lower priority won't be in effect.)
* roleName: The name of the role.
* commandRate: This identifies whether the role gives permission to use the !rate command. (0 = no permissions to use; 1 = permission to use.)
* commandFeature: This identifies whether the role gives permission to use the !feature command. (0 = No permissions to use; 1 = permission to use.)
* commandEpic: This identifies whether the role gives permission to use the !epic command. (0 = no permissions to use; 1 = permission to use.)
* commandUnepic: This identifies whether the role gives permission to use the !unepic command. (0 = no permissions to use; 1 = permissions to use;)
* commandVerifyCoins: This identifies whether the role gives permission to use the !verifycoins command. (0 = no permissions to use; 1 = permissions to use.)
* commandDaily: This identifies whether the role gives permission to use the !daily command. (0 = no permissions to use; 1 = permissions to use.)
* commandWeekly: This identifies whether the role gives permission to use the !weekly command. ( 0 = no permissions to use; 1 = permissions to use.)
* commandDelete: This identifies whether the role gives permission to use the !delete command. (0 = no permissions to use; 1 = permissions to use.)
* commandSetacc: This identifies whether the role gives permission to use the !setacc command. (0 = no permissions to use; 1 = permissions to use.)
* commandRenameOwn: This is always 1 by default even without a role. This allows users to use the !rename command on their levels.
* commandRenameAll: This identifies whether the role give permission to use the !rename command on any level. (0 = no permissions to use; 1 = permissions to use.)
* commandPassOwn: This is default set to 1 for users without a role even. This allows users to use the !pass command on their own levels.
* commandPassAll: This identifies whether the role gives permission to use the !pass command on any level. (0 = no permissions to use; 1 = permissions to use.)
* commandDescriptionOwn: This is default set to 1 for all users, even without a role. This allows users to use the !description command on their own levels.
* commandDescriptionAll: This identifies whether the role gives permission to use the !description command on any level. (0 = no permissions to use; 1 = permissions to use.)
* commandUnlistOwn: This is default set to 1 for all users, even users without a role. This allows users to use the !unlist command on their own levels.
* commandUnlistALll: This identifies whether the role gives permission to use the !unlist command on any level. (0 = no permissions to use; 1 = permissions to use.)
* commandShareCpOwn: This is default set to 1 for all users, even users without a role. This allows users to use the !sharecp command on their own levels.
* commandShareCpAll: This identifies whether the role gives permission to use the !sharecp command on any level. (0 = no permissions to use; 1 = permissions to use.)
* commandSongOwn: This is default set to 1 for all users, even users without a role. This allows users to use the !song command on their own levels.
* commandSongAll: This identifies whether the role gives permission to use the !song command on any level. (0 = no permissions to use; 1 = permissions to use.)
* profilecommandDiscord: I am not sure if this even works anymore.
* actionRateDemon: This is the defualt rate button that all users have. It is default set to 1 for all users.
* actionRateDifficulty: This is the default rate button that all users have. It is default set to 1 for all user.
* actionRequestMod: This is the normal req button in settings. All users have permission to use this by default.
* actionSuggestRating: This identifies whether the role gives you permission to use the blue star moderator button. If you made your role correctly and didn't want the role to rate levels, it will suggest a rating for a level and send it to "suggestlist.php" in your tools page. If you have !rate command permissions or just suggest rate permissions(given from GDPSFH webpanel) you can rate levels with this button. (0 = no permissions to use it; 1 = permission to use it.)
* actionDeleteComment: This identifies whether the role gives you permission to delete any comment. (0 = no permission to delete; 1 = permission to delete.)
* toolLeaderboardsBan: This identifies whether the role gives you permission to use leaderboardsban.php in your GDPS tools page. (0 = no permission to use; 1 = permission to use.)
* toolPackCreate: This identifies whether the role gives you permission to use packCreate.php in your Tools page. (0 = no permission to use it; 1 = permission to use it.)
* toolQuestsCreate: This identifies whether the role gives you permission to use addQuests.php in your tools page. (0 = no permission to use; 1 = permission to use.)
* toolModActions: This identifies whether the role gives you permission to use modActions.php in your tools page. (0 = no permission to use; 1 = permission to use.)
* toolSuggestList: This identifies whether the role gives you permission to use suggestList.php in your tools page. (0 = no permission to use; 1 = permission to use.)
* dashboardModTools: This identifies whether the role gives you permission to use the moderator tools on the dashboard (beta). (0 = no permission to use; 1 = permission to use.)
* modipCategory: This identifies whether the role gives you access to the free copy permission. (You put the category ID of the modip category you created in modipperms.)
* isDefault: I am not sure about what this does. (It does not make the permissions of the role default to any member.)
* commentColor: This displays what colour the comments will be if you have this role. (It is in RGB color code)
* modBadgeLevel: This is the level of the moderator badge. (0 = no badge; 1 = Normal Moderator badge; 2 = Elder Moderator badge; 3 = Leaderboard moderator badge Note: Putting this badge as the role badge doesn't allow you to press req in-game as req will infinitely load and never succeed.)

### Songs: This table lists all the custom uploaded songs and the songs used in the GDPS.

* ID: The unique ID of the song.
* name: The name of the song that will appear in-game.
* authorID: The unique ID of the author of the song. (Newgrounds author ID.)
* size: The size of the song that will display when downloading the song and using it. (It won't always be the actual size of the song as the default is 6.69mb.)
* download: The download link for the song that you download from in-game.
* hash: unused
* isDisabled: This identifies whether the song is availible to download or not. (0 = not disabled; 1 = disabled.) It will return "song is not allowed for use" in-game if you download a song that has "isDisabled" set to 1.
* levelsCount: The amount of uploaded levels that use this song.
* reuploadTime: Supposed to display the time the song was uploaded in unix timestamp format. (It doesn't appear to work.)

### Suggest: This table lists all levels moderators have used the suggest rate button on.(If they didn't rate the level using the button.)

* ID: The unique ID of the suggest.
* suggestBy: The account ID of the user who suggested to rate this level.
* suggestLevelID: The ID of the level that was suggested by the user.
* suggestDifficulty: This tells you what difficulty was suggested. ( 0 - N/A; 10 - Easy; 20 - Normal; 30 - Hard; 40 - Harder; 50 - Insane/Demon/Auto.)
* suggestStars: The amount of stars (value) that were suggested. (Example: 7)
* suggestFeatured: This identifies if the level was suggested for a feature or not. (0 = Suggested for a standard rate; 1 = suggested for feature.)
* suggestAuto: This identifies if the level was suggested to be rated auto difficulty or not. (0 = not auto difficulty; 1 = auto difficulty.)
* suggestDemon: This identifies if the level was suggested to be rated demon difficulty or not. (0 = not demon difficulty; 1 = demon difficulty.)
* timestamp: This displays the time the level was suggested at in unix timestamp format. (You can use an online converter to find out the exact date.) (**Note: Unless you set your role up correctly, the suggest table will be empty as normal moderators will be able to rate levels with the suggest rate button.**)

### Users: This table lists all the users in the GDPS (registered accounts and green users.)

* isRegistered: This identifies if the user has registered an account or not. (0 = not registered; 1 = registered account.)
* userID: This is the unique ID of each user.
* extID: This is the user's account ID, if they are registered.
* userName: This is the users name.
* stars: This is the amount of stars the user has.
* demons: This is the amount of demons the user has completed.
* icon: This is the icon the user is using. (Icons have unique ID's too.)
* color1: This is the primary color of the user's icons. (colors also have unique ID's.)
* color2: This is the secondary color of the user's icons. (colors have unique ID's.)
* iconType: This is the type of icon that will appear behind the user's name when they comment and when you search up the user. (0 = cube; 1 = ship; 2 = ball; 3 = ufo; 4 = wave; 5 = robot; 6 = spider.)
* coins: This is the amount of secret coins the user has collected.
* userCoins: This is the amount of user coins the user has collected.
* special: I am not sure about what this is or what it is meant to display.
* gameVersion: The version of the game the user is using. (21 is 2.1, 20 is 2.0, 19 is 1.9 and so on.)
* secret: This is not very secret. Everyone's secret is Wmfd2893gb7.
* accIcon: This is the ID of the icon the user is using.
* accShip: This is the ID of the ship the user is using.
* accBall: This is the ID of the ship the user is using.
* accBird: This is the ID of the ufo the user is using. (The ufo was originally called the bird.)
* accDart: This is the ID of the wave the user is using. (The wave was originally called the dart.)
* accRobot: This is the ID of the robot the user is using.
* accGlow: This is to identify if the user has glow arounf their icons. (0 = no glow; 1 = glow.)
* creatorPoints: This is the amount of creator points the user has gained from rated levels.
* IP: This is the IP address of the person who made the user.
* lastPlayed: This is the date and time of the last time the person went into the GDPS, in unix timestamp format. (You can use an online converter to get the exact date and time.)
* diamonds: This is the amount of diamonds the user has collected.
* moons: Amount of moons the user collected (2.2)
* orbs: This is the amount of orbs the user has collected.
* completedLvls: This shows the amount of levels the user has completed.
* accSpider: This is the unique ID of the user's spider. (I also don't know why accSpider is so far away from the other icons.)
* accExplosion: This is the unique ID of the user's death effect.
* chest1time: This is the date and time since the user opened the small chest. (It is in unix timestamp format in which you can use an online converter to get the exact date.)
* chest2time: This is the date and time since the user opened the big chest. (It is in unix timestamp format in which you can use an online converter to get the exact date.)
* chest1count: This is the amount of times the user has opened the small chest.
* chest2count: This is the amount of times the user has opened the big chest.
* isBanned: This identifies whether the user is leaderboard banned on the stars leaderboard on that account or not. (0 = not stars leaderboard banned; 1 = stars leaderboard banned.)
* isCreatorBanned: This identifies whether the user is leaderboard banned on the creator points leaderboard on that account or not. (0 = not creator leaderboard banned; 1 = creator leaderboard banned.)

## Examples of using a table.

An example with using a table and its columns would be this:

Roles table: Click insert, set the permissions to 1 or 0, set the name and set the unique ID. Now click go.

Now go to the roleassign table: click insert, set the unique assign ID, put in the account ID you want to assign the role to and now put the ID of the role you are going to assign.

Now click go at the bottom of the site.

I hope this guide helped you to understand PhpMyAdmin better.

#### Extra Information:

If someone tells you to login to PMA, that means you must login to phpMyAdmin.

You do not need to know PHP to use phpMyAdmin.

Guide made by Nojnis, with help from Wyliemaster's gd-docs documentation, [Wyliemaster's GD documentation here](https://github.com/Wyliemaster/gddocs) and thanks to Migmatos for helping with a couple columns.

PS: I will update the information about the functions of columns I didn't know about when I find out.
(If you have any more questions, ping Nojnis is the discord.)
