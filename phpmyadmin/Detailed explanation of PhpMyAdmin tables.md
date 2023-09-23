# An In-depth explanation of the PhpMyAdmin tables

## Acccomments: This table displays all the account comments players have made on their profiles.
  userID: Tells you what user ID made the comment.
  Comment: Displays the content of the account comment. (it is encrypted though)
  Secret: Unused
  CommentID: Unique ID of the account comment.
  Timestamp: The unix timestamp. (basically when the comment was uploaded. You can use an online calculator to see the actual date and time.)
  Likes: displays how many likes it has. (A negative likes amount means dislikes.)
  isSpam: Shows if the comment has enough dislikes to be marked as spam
## Accounts: This table displays all the accounts in the GDPS.
  userName: Tells you the account's username it was registered with.
  password: Gives you password hash for the password of their account. (You can't decrypt this information, you can only use a website to check if the hash corresponds to text you type.)
  gjp2: Encrypted password hash
  email: Displays the email the account was registered with.
  accountID: Unique ID of the account. (useful when something in PhpMyAdmin asks for accountID.)
  isAdmin: This adds all permissions to your GDPS account.
  mS: This is the message state of the account. It doesn't appear to work though.
  frS: This is the friend request state of the account. It doesn't appear to work though.
  cS: This is the comment state(who to show your comment history to). It doesn't appear to work though.
  youtubeurl: The YouTube account URL the user has linked to their profile. (It only shows you what you put after the / in youtube.com/. Example: youtube.com/GoogleDrive.)
  twitter: The Twitter(X) account URL the user has linked to their profile. (Again it only shows you what to put after the / in twitter.com URL. Example twitter.com/discord.)
  twitch: The Twitch account the user has linked to their profile. (This only tells you what to put after the / in twitch.tv URL. Example: twitch.tv/epicgamer.)
  salt: It doesn't appear to do anything. It's blank for every account.
  registerDate: Tells you what date the user registered their account in unix timestamp format. (Use a online calculator to find the actual date the account was registered on.)
  friendsCount: Displays the amount of friends the user has added on their account.
  discordID: I think this was used for the discontinued Cvolton GDPS bot.
  discordLinkRequest: Also used for discontinued Cvolton GDPS bot.
  isActive: Will either be 0 or 1. 0 means the account is not activated while 1 means the account is activated.
## Actions: This table will display automatic server-side actions.
  ID: This tells you what account ID either did the action or received the automatic server-side action or just the ID of the action if it was not an action for an account.
  type: This tells you the type of action that was issued. I am not 100% sure about what action is what number. (I will update this when I find out.)
  value: This tells you what if the action happened on an account, level and anything else. (It will tell you a username for an account, a level ID for a level action and not sure about the other ones.
    I will ipdate the guide when I find out.)
  timestamp: the unix timestamp of when the action happened. ( You can use an online calculator to tell you when it was exactly.)
  value2: A column that tells you the IP of the account the action was issued to. (It is for more than just that but I'm unsure so I will update this guide when I find out.)
  value3: A column I'm not sure of again. ( I will update this guide when I find out.)
  value4: Not sure. (I will update this guide when I find out.)
  value5: Not sure again. (I will update this guide when I find out.)
  value6: Not sure still. (I will update this guide when I find out.)
  account: I'm not sure but I think it is to tell you whether the action was to do with an account. ( I will update this guide when I find out.)
## Actions_downloads: This table lists every level download. It doesn't count another download when a user downloads a level again.
  id: This is the unique ID for the download of the level.
  levelID: This tells you what level ID was downloaded.
  ip: This tells you the IP of the user who downloaded the level. It is in varbinary(4) format.
  uploadDate: Displays the date and time the level was downloaded in a normal format. (Year-Day-Month-Hours-Minutes-Seconds.)
## Actions_likes: This table lists every level a user has liked.
  id: This is the unique ID for the like on a level.
  itemID: This is the level ID that was liked.
  type: the type of like. 1 = level, 2 = comment on a level and 3 = account comment.
  isLike: Tells you whether it was a like or a dislike. 0 = dislike and 1 = like.
  ip: This is the IP of the user who liked the level. It is in varbinary(4) format.
  uploadDate: The date and time of when the level was liked. It is displayed in normal format. Year-Day-Month-Hours-Minutes-Seconds.
## Bannedips: this table displays what IP addresses are leaderboard banned.
  ID: The unique ban ID.
  IP: The IP you want to leaderboard ban.
## Blocks: This table lists any users who have blocked each other
  ID: The unique ID of the block.
  person1: the Account ID of the user who clicked "block" button.
  person2: the Account ID of the user who "person1" blocked.
## Comments: This table lists comments on levels.
  userID: The ID of the user who commented.
  userName: The username of the user ID who commented on the level.
  Comment: This displays the content of the uploaded comment. (It is base64 encoded and you can decode it to see the content too.)
  Secret: None
  levelID: The ID of the level that the comment was made on.
  commentID: Unique ID of a comment.
  timestamp: The unix timestamp of when the comment was uploaded. (You can use an online converter to get the actual date.)
  likes: The amount of likes on the comment.
  percent: The percent the user got on the level when they uploaded the comment.
  isSpam: This will only be 1 if the comment has a lot of dislikes. (0 is not spam and 1 is spam.)
## Cpshares: This is the table that lists all the levels !sharecp command was used on.
  shareID: This is the unique ID of the Creator Points share.
  levelID: the ID of the level you used !sharecp on.
  userID: The ID of the user you shared the Creator Points with.
## Dailyfeatures: This table lists all the daily and weekly levels.
  feaID: The unique ID of the daily/weekly level.
  levelID: The ID of the level that is daily/weekly.
  timestamp: This is the unix timestamp of when the level was made daily/weekly. (You can use an online converter to get an actual date.)
  type: The type. It can only be daily or weekly. 0 is daily and 1 is weekly.
## Friendreqs: This table lists all the friend requests that have been sent.
  accountID: The ID of the account that sent the friend request.
  toAccountID: The ID of the account that the friend request was sent to.
  comment: This displays the message that someone sent with the friend request. (It might be blank for some friend requests sent because the user didn't attach a message with it.)
  uploadDate: The unix timestamp of when the friend request was sent. (You can use an online converter to see the actual date.)
  ID: The unique ID of the friend request.
  isNew: It will be either 0 or 1. 0 meaning the user sent a friend request before and 1 being the user hasn't sent a friend request before.
## Friendships: This table lists all the users who have added each other as friends.
  ID: The unique ID of the friendship.
  person1: The account ID of the person who accepted the friend request
  person2: The account ID of the person who sent the friend request.
  isNew1: It will be 0 or 1. 0 meaning it is not new and the user has added the other person as a friend before and 1 meaning it is new. (This is for person 1 too.)
  isNew2: The same as isNew1, just for person 2.
## Gauntlets: This table lists the gauntlets and allows you to make gauntlets.
  ID: The ID of the guantlets. (1 = fire, 2 = fire, 3 = poison, etc.) It follows real Geometry Dash's order of gauntlets.
  level1: The first level.
  level2: The second level.
  level3: The third level.
  level4: The fourth level.
  level5: The Fifth level.
    (Note: The levels will be ordered by difficulty so if you put a 4 star as level1 and a 2 star as level2, level 1 will be the 2 star.)
## Levels: This table lists all the uploaded levels in the GDPS.
  gameVersion: This is the version of the game the level was made and uploaded in. (21 means version 2.1, 20 would mean version 2.0 and so on.)
  
  
  
  
  
  
  
  

