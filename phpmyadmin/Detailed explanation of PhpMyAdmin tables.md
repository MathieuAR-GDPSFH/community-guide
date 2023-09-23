# An In-depth explanation of the PhpMyAdmin tables

## Acccomments: This table displays all the account comments players have made on their profiles.
- userID: Tells you what user ID made the comment.
  
- Comment: Displays the content of the account comment. (it is encrypted though)
  
- Secret: Unused
  
- CommentID: Unique ID of the account comment.
  
- Timestamp: The unix timestamp. (basically when the comment was uploaded. You can use an online calculator to see the actual date and time.)
  
- Likes: displays how many likes it has. (A negative likes amount means dislikes.)
  
- isSpam: Shows if the comment has enough dislikes to be marked as spam

## Accounts: This table displays all the accounts in the GDPS.
  
- userName: Tells you the account's username it was registered with.
 
- password: Gives you password hash for the password of their account. (You can't decrypt this information, you can only use a website to check if the hash corresponds to text you type.)
  
- gjp2: Encrypted password hash
  
- email: Displays the email the account was registered with.

- accountID: Unique ID of the account. (useful when something in PhpMyAdmin asks for accountID.)

- isAdmin: This adds all permissions to your GDPS account.

- mS: This is the message state of the account. It doesn't appear to work though.

- frS: This is the friend request state of the account. It doesn't appear to work though.

- cS: This is the comment state(who to show your comment history to). It doesn't appear to work though.

- youtubeurl: The YouTube account URL the user has linked to their profile. (It only shows you what you put after the / in youtube.com/. 
  Example: youtube.com/GoogleDrive.)

- twitter: The Twitter(X) account URL the user has linked to their profile. (Again it only shows you what to put after the / in twitter.com URL. 
  Example twitter.com/discord.)

- twitch: The Twitch account the user has linked to their profile. (This only tells you what to put after the / in twitch.tv URL. 
  Example: twitch.tv/epicgamer.)
 
- salt: It is useless for accounts.

- registerDate: Tells you what date the user registered their account in unix timestamp format. (Use a online calculator to find the actual date the account was registered on.)

- friendsCount: Displays the amount of friends the user has added on their account.

- discordID: I think this was used for the discontinued Cvolton GDPS bot.

- discordLinkRequest: Also used for discontinued Cvolton GDPS bot.

- isActive: Will either be 0 or 1. 0 means the account is not activated while 1 means the account is activated.

## Actions: This table will display automatic server-side actions.

- ID: This tells you what account ID either did the action or received the automatic server-side action or just the ID of the action if it was not an action for an account.

- type: This tells you the type of action that was issued. I am not 100% sure about what action is what number. (I will update this when I find out.)
 
- value: This tells you what if the action happened on an account, level and anything else. (It will tell you a username for an account, a level ID for a level action and not sure about the other ones.
  (I will update the guide when I find out.)
 
- timestamp: the unix timestamp of when the action happened. ( You can use an online calculator to tell you when it was exactly.)
  
- value2: A column that tells you the IP of the account the action was issued to. (It is for more than just that but I'm unsure so I will update this guide when I find out.)
  
- value3: A column I'm not sure of again. ( I will update this guide when I find out.)
  
- value4: Not sure. (I will update this guide when I find out.)
  
- value5: Not sure again. (I will update this guide when I find out.)
  
- value6: Not sure still. (I will update this guide when I find out.)
  
- account: I'm not sure but I think it is to tell you whether the action was to do with an account. ( I will update this guide when I find out.)

## Actions_downloads: This table lists every level download. It doesn't count another download when a user downloads a level again.
  
- id: This is the unique ID for the download of the level.
  
- levelID: This tells you what level ID was downloaded.
 
- ip: This tells you the IP of the user who downloaded the level. It is in varbinary(4) format.
  
- uploadDate: Displays the date and time the level was downloaded in a normal format. (Year-Day-Month-Hours-Minutes-Seconds.)

## Actions_likes: This table lists every level a user has liked.
 
- id: This is the unique ID for the like on a level.
  
- itemID: This is the level ID that was liked.
  
- type: the type of like. 1 = level, 2 = comment on a level and 3 = account comment.
  
- isLike: Tells you whether it was a like or a dislike. 0 = dislike and 1 = like.
  
- ip: This is the IP of the user who liked the level. It is in varbinary(4) format.
  
- uploadDate: The date and time of when the level was liked. It is displayed in normal format. Year-Day-Month-Hours-Minutes-Seconds.

## Bannedips: this table displays what IP addresses are leaderboard banned.
  
- ID: The unique ban ID.
  
- IP: The IP you want to leaderboard ban.

## Blocks: This table lists any users who have blocked each other
  
- ID: The unique ID of the block.
  
- person1: the Account ID of the user who clicked "block" button.
  
- person2: the Account ID of the user who "person1" blocked.

## Comments: This table lists comments on levels.
 
- userID: The ID of the user who commented.
 
- userName: The username of the user ID who commented on the level.
  
- Comment: This displays the content of the uploaded comment. (It is base64 encoded and you can decode it to see the content too.)

- Secret: None

- levelID: The ID of the level that the comment was made on.

- commentID: Unique ID of a comment.
  
- timestamp: The unix timestamp of when the comment was uploaded. (You can use an online converter to get the actual date.)
  
- likes: The amount of likes on the comment.
  
- percent: The percent the user got on the level when they uploaded the comment.
  
- isSpam: This will only be 1 if the comment has a lot of dislikes. (0 is not spam and 1 is spam.)

## Cpshares: This is the table that lists all the levels !sharecp command was used on.

- shareID: This is the unique ID of the Creator Points share.
  
- levelID: the ID of the level you used !sharecp on.
  
- userID: The ID of the user you shared the Creator Points with.

## Dailyfeatures: This table lists all the daily and weekly levels.

- feaID: The unique ID of the daily/weekly level.
  
- levelID: The ID of the level that is daily/weekly.
  
- timestamp: This is the unix timestamp of when the level was made daily/weekly. (You can use an online converter to get an actual date.)
  
- type: The type. It can only be daily or weekly. 0 is daily and 1 is weekly.

## Friendreqs: This table lists all the friend requests that have been sent.

- accountID: The ID of the account that sent the friend request.
  
- toAccountID: The ID of the account that the friend request was sent to.
  
- comment: This displays the message that someone sent with the friend request. (It might be blank for some friend requests sent because the user didn't attach a message with it.)
  
- uploadDate: The unix timestamp of when the friend request was sent. (You can use an online converter to see the actual date.)
  
- ID: The unique ID of the friend request.
  
- isNew: It will be either 0 or 1. 0 meaning the user sent a friend request before and 1 being the user hasn't sent a friend request before.

## Friendships: This table lists all the users who have added each other as friends.
  
- ID: The unique ID of the friendship.
  
- person1: The account ID of the person who accepted the friend request
  
- person2: The account ID of the person who sent the friend request.
  
- isNew1: It will be 0 or 1. 0 meaning it is not new and the user has added the other person as a friend before and 1 meaning it is new. (This is for person 1 too.)
  
- isNew2: The same as isNew1, just for person 2.

## Gauntlets: This table lists the gauntlets and allows you to make gauntlets.
  
- ID: The ID of the guantlets. (1 = fire, 2 = fire, 3 = poison, etc.) It follows real Geometry Dash's order of gauntlets.
  
- level1: The first level.

- level2: The second level.
  
- level3: The third level.
  
- level4: The fourth level.
  
- level5: The Fifth level.
  
  (Note: The levels will be ordered by difficulty so if you put a 4 star as level1 and a 2 star as level2, level 1 will be the 2 star.)

## Levels: This table lists all the uploaded levels in the GDPS.
  
- gameVersion: This is the version of the game the level was made and uploaded in. (21 means version 2.1, 20 would mean version 2.0 and so on.)

- binaryVersion: This is supposed to be the update version not the game version. Although it does not display properly.

- userName: This is the username of the creator of the level.

- levelID: This is the unique ID of the level.

- levelName: This displays what the level is called in-game.

- levelDesc: This displays the contents of the level description is. (It is base64 encoded and you can decode it.)

- levelVersion: The version of the level.

- levelLength: The length of the level. (0 = Tiny; 1 = Short; 2 = Medium; 3 = Long; 4 = XL.)

- audioTrack: This tells you the ID of the music, if it is a default song used.

- auto: This will mean the level is rated auto if it is 1. 0 means it is not rated auto.

- password: The level copy password. (If there is no password it will be 0.)

- original: This will either be 0 or the ID of the original level that it was copied from.

- twoPlayer: This displays either 0 or 1. 0 being the level is not 2 player and 1 being the level is 2 player.

- songID: This displays the ID of the custom song used.

- objects: This displays the amount of objects the level has.

- coins: This displays how many coins the level has. (It ranges from 0 - 3)

- requestedStars: The amount of stars requested when the level was uploaded.

- extraString: This is a complicated topic to explain here but basically it is other objects and layers of objects and much more. 
  Here is a link to [the detailed explanation](https://github.com/Wyliemaster/gddocs/blob/master/docs/resources/client/level-components/capacity-string.md).

- levelString: This is empty as I don't think it is used. (I will update this if it is used or was used.)

- levelInfo: This displays the level's code. (If you look in CCLocalLevels.dat file, level code will look like this too.)

- secret: This is used to identify if you are using a Geometry Dash client to upload levels or if you are using an external client.
  For more information about secrets [check out this documentation.](https://github.com/Wyliemaster/gddocs/blob/master/docs/reference/secrets.md)

- starDifficulty: This displays what difficulty the level is. (0 = N/A; 10 = Easy; 20 = Normal; 30 = Hard; 40 = Harder; 50 = Insane; 50 = Auto; 50 = Demon;)

- downloads: This displays the amount of downloads the level has.

- likes: This displays how many likes the level has.

- starDemon: This is used to identify if the level is a demon or not. 0 = not demon and 1 = demon.

- starAuto: This is used to identify if the level is star auto rated or not. 0 = not auto 1 is auto.

- starStars: This is used to display how many stars the level is rated. (Example: 10)

- uploadDate: This is the date the level was uploaded in unix timestamp form. (You can use an online converter to get the exact date.)

- updateDate: This is the date the level was updated in unix timestamp form0. (You can use an online converter to get the exact date.) If the level was never updated then this will be the upload date.

- rateDate: The date the level was rated in unix timestamp form. (You can use an online converter to get the exact date.) It will be either the star or no star rate date.

- starCoins: This tells you if the coins are verified or not. (0 = not verified coins; 1 = verified coins.)
  <mark style="color:red;">**DO NOT SET starCoins TO 2 OR HIGHER AS IT WILL BREAK YOUR LEVELS TAB!**</mark>

- starFeatured: This indetifies whether the level is featured or not. (0 = not featured; 1 = featured.)

- starHall: This identifies whether the level goes into the "Hall of Fame" tab or not. 0 = Not in Hall of Fame; 1 = In Hall of Fame.

- starEpic: This identifies whether the level is epic rated or not. (0 = Not epic rated; 1 = The level is epic rated.)

- starDemonDiff: This tells you what demon difficulty the level is rated. (0 = Non-demon rated levels; 1 = Easy demon; 2 = Medium Demon; 3 = Hard Demon; 4 = Insane Demon; 5 = Extreme Demon.)

- userID: The ID of the user who uploaded the level.

- extID: The account ID of the user who uploaded the level.

- unlisted: This tells you whether the level is unlisted or not. (0 = public; 1 = unlisted.)

- originalReupload: Only displays a level ID of the original level if you re-uploaded a level from another GDPS using reupload.php.
  (It will be the GDPS you re-uploaded the level from, original level ID)

- hostname: The IP address of the level uploader.

- isCpShared: This identifies whether the !sharecp command was used on the level.

- isDeleted: This identifies whether the level is deleted from the servers but is still in the database. (0 = not deleted; 1 = deleted.)

- isLDM: This identifies whether the level has an LDM button or not. (0 = No LDM button; 1 = LDM button.)

- unlisted2: Tells you if the level is unlisted and availible for public as long as users have the ID. (I think I'm not 100% sure yet.)

- wt: I am not sure (I will find out and update this.)

- wt2: also not sure.

- settingsString: Unused.

## Levelscores: This table lists the percentages players have got on levels.

- scoreID: This is a unique ID to each score.

- accountID: The ID of the account that got the score.

- levelID: The ID of the level the user got the score on.

- percent: The percentage the user got on the level.

- uploadDate: The date in which the user got the score in unix timestamp format. (You can use an online converter to find the exact date.)

- attempts: The amount of attempts the user took to get the percentage on the level.

- coins: The amount of coins collected (if applicable). (Ranges from 0 - 3.)

- clicks: The amount of times the user clicked when they got the percent on the level.

- time: The amount of time it took for the user to get the percentage on the level.

- progresses: The percentages achieved before the user's highest percentage on the level.

- dailyID: The daily ID of the daily level they got a percentage on.
  (Only applicable if the user actually got a percentage on a daily level.)

## Links: This tables displays any servers you have used linkaccount.php with

- ID: The unique ID of the link

- accountID: Your GDPS account ID.

- targetAccountID: The account ID on the server you linked your account to.

- server: The server you linked your account to.

- timestamp: The date you linked the account in unix timestamp format. (You can use an online converter to get the exact date.)

- userID: The ID of your GDPS user.

- targetUserID: The ID  of your user in the other server.
  (**Note: linkaccount.php only works between other GDPS's**)

## Mappacks: This table lists the map packs that are created in the GDPS and allows you to create Map packs.

- ID: The unique ID of the map pack.

- name: The name of the map pack.

- levels: The ID's of the levels in the map pack.

- stars: The amount of stars the map pack will give.

- coins: The amount of secret coins the map pack will give.

- difficulty: The difficulty face that will show up on the map pack in-game.
  (0 = auto; 1 = Easy; 2 = Normal; 3 = Hard; 4 = Harder; 5 = Insane; 6 = Demon.)

## Messages: This table displays all the messages sent to other users from other users.

- userID: The ID of the user sending the message.

- userName: The username of the user sending the message.

- body: The body of the message sent. (It is base64 encoded, you can decode this text though.)

- subject: The subject of the sent messages. (Also base64 encoded.)

- accID: The ID of the account sending the message.

- messageID: The unique ID of the message.

- toAccountID: This tells you the account ID the message was sent to.

- timestamp: This tells you when the message was sent in unix timestamp format. (You can use an online converter to see the exact date.)

- secret: Read [this documentation for more information.](https://github.com/Wyliemaster/gddocs/blob/master/docs/reference/secrets.md)

- isNew: This displays whether the message is new and that the user hasn't sent a message to the user before. (0 = sent message before; 1 = never sent message before.)

## Modactions: This table lists all the actions done by moderators in-game.

-  ID: Unique ID for all moderator actions.

-  type: this has many different types, whether it is from rating a level to deleting a level.
   (1 = rating a level a demon, or any other difficulty using !rate command; 2 = featuring a level; 3 = When you verify coins; 4 = rating a level non-demon;
   5 = unsure; 6 = Using !delete on a level; 7 = using !setacc on a level; 8 = using !rename on a level; 9 = Not sure for now; 10 = using demon moderator rate button;
   11 = creating a map pack from tools page; 15 = I am unsure currently; 16 = using !song command on a level and changing it's song ID; 25 = creating a quest.
   I think that is all the types, well the ones I know about for now. I will update this when I get all the information.)

- Value: this depends on the action but if you look at certain actions it will display the following:

  1: Rating a level demon or other difficulties using !rate command displays: [Difficulty].

  2: Featuring a level will display 1 or 0
  (depending on what you typed with !feature, if you just typed "!feature", it'll make it 1, if you type "!feature 0" it will display 0 and also un-feature the level.)

  3: Verifying the coins of a level will display 1 under values column.

  4: This will display a 1 when you do !epic and it will display a 0 if you do !unepic.

  5: Not 100% sure yet

  6: It will display a 1 if you used !delete on a level.

  7: It will display the username of the account you set a level to using !setacc command.

  8: It will display the new name of the level after using !rename on an level.

  9: unsure

  10: It will display Easy,Medium,Hard,Insane or Extreme here depending on the demon difficulty you set it to using the demon rate moderator button.

  11: It will display the name of the map pack here if you used packcreate.php for a map pack from tools page.

  15: unsure

  16: It will display the new song ID of the level you used the !song command on a level.

  25: it will display the ID of what you need to get for a quest. (later on you will see the ID's of orbs, diamonds and stars for the quests table.)

- timestamp: This displays the date and time the action was issued on in unix timestamp format. (You can use an online converter to get exact date.)

- value2: This displays other values, it can display the amount of orbs,diamonds or stars required for a quest, and more.



  

  

  

  
  
  
  
  
  
  
  

