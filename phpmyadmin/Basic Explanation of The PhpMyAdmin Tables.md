# PhpMyAdmin tables
- PhpMyAdmin looks very confusing when you first see it, with all the tables.
- Well here isva basic explanation of the tables.

• Acccomments: this table lists all the account comments, shows you the account ID of the user who uploaded the comment.
• Accounts: What the name says, lists all the accounts, their account ID's, usernames and if the account is active. 
  Password section gives you password hash which doesn't actually give you the account password.
• Actions: This table lists actions such as mod actions, also lists other actions such as a disabled account.
• Actions_downloads: this table counts downloads per IP per level.
• Actions_likes: The table counts likes per IP per level.
• Bannedips: To IP ban someone from leaderboards.
• Blocks: lists who has blocked who in your GDPS.
• Comments: Lists every comment, tells you what account ID uploaded the comment, and what level ID it was commented on.
  Tells you the comment ID too.
• Cpshares: shows what levels !sharecp command was used on, along with the users.
• Dailyfeatures: lists all the daily levels that have been set.
• Friendreqs: Lists all the friend requests sent to users from another user.
• Friendships: Lists all the users who are friends.
• Gauntlets: Lists all the gauntlets in the GDPS, it also allows you to create them.
• Levels: Lists all the levels, shows all the information about them.
• Levelscores: Lists what account ID had what percentage on what level ID.
• Links: Lists every user who has added some link to their profile, (YouTube link, Twitter, etc).
• Mappacks: Lists all the map packs, also another way to create map packs instead of tools page.
• Messages: lists all the messages sent to users. The content is encoded.
• Modactions: Lists all actions done by mods, whether its suggesting a rate, featuring a level, it'll all go here.
• Modipperms: I am actually not sure how this works exactly, but I think, if a ID (not account ID) is added here
  and actionFreeCopy is set to 1, the mod can copy any level without mods(not 100% sure yet).
• Modips: Lists moderators IP's.
• Quests: Lists all the quests, you can also create and delete quests here too.
• Reports: lists any levels that have been reported.
• Roleassign: The way to assign a role to your account in PhpMyAdmin, after creating a role.
• Roles: Lists every created role, you can create roles here too.
• Songs: Lists all reuploaded songs in the GDPS.
• Suggest: Lists levels moderators have used suggest rate on and haven't rated
  ^^^ (Not working I don't think because giving a role suggest rate, allows the user to rate levels with the moderator button).
• Users: Lists all the users, gives you user ID, IP, and so much more.
  You can star only leaderboard ban someone in this table by setting isBanned to 1 but leaving isCreatorBanned at 0.
  There's a lot of info in this table.
___________________________________________________________________________________________

Hope this helped
