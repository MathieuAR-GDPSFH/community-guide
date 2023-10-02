# Basic explanation of phpMyAdmin tables

• Acccomments: this table lists all the account comments, shows you the account ID of the user who uploaded the comment and the time the comment was uploaded.

• Accounts: What the name says, lists all the accounts, their account ID's, usernames and if the account is active. Password section gives you password hash which doesn't actually give you the account password.

• Actions: This table lists actions such as mod actions, also lists other actions such as a disabled account.

• Actions\_downloads: this table counts downloads per IP per level. (It does not count downloading a level again.)

• Actions\_likes: The table counts likes per IP per level.

• Bannedips: To IP ban someone from leaderboards.

• Blocks: lists who has blocked who in your GDPS.

• Comments: Lists every comment, tells you what account ID uploaded the comment, and what level ID it was commented on. Tells you the comment ID too.

• Cpshares: shows what levels !sharecp command was used on, along with the users.

• Dailyfeatures: lists all the daily and weekly levels that have been set.

• Friendreqs: Lists all the friend requests sent to users from another user.

• Friendships: Lists all the users who are friends.

• Gauntlets: Lists all the gauntlets in the GDPS, it also allows you to create them.

• Levels: Lists all the levels, shows all the information about them.

• Levelscores: Lists what account ID had what percentage on what level ID.

• Links: Used for the tools linkAcc.php tool to set who owns the level when a user re-uploading level.

• Mappacks: Lists all the map packs, also another way to create map packs instead of tools page.

• Messages: lists all the messages sent to users (The content is encoded in base64).

• Modactions: Lists all actions done by mods, whether its suggesting a rate, featuring a level, it'll all go here.

• Modipperms: Special permissions for moderators, currently only for the purpose of allowing copying every level.

• Modips: Lists moderators IP's.

• Quests: Lists all the quests, you can also create and delete quests here too.

• Reports: lists any levels that have been reported.

• Roleassign: The way to assign a role to your account in PhpMyAdmin, after creating a role.

• Roles: Lists every created role, you can create roles here too.

• Songs: Lists all reuploaded songs in the GDPS.

• Suggest: Lists levels moderators have used suggest rate on.(only works if you've configured your role correctly).

• Users: Lists all the users, gives you user ID, IP, and so much more. You can star only leaderboard ban someone in this table by setting isBanned to 1 but leaving isCreatorBanned at 0. There's a lot of info in this table.

***

Hope this helped.
