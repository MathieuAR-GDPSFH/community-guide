# Give Permissions to users

This guide will cover how to give users moderator or custom permissions using pfpmyadmin

1. Open phpMyAdmin and log in
2. Select the database starting with "gdps_"
3. Look for "roles"
4. Open the Insert Tab
5. Fill in these things
      • roleID: The ID of the role
      • priority: the priority the role has over other roles
      • roleName: the name of the role (Note: it will not display im game)
6. setup your pernissions, the table below explains them (NOTE: Set **1** to grant the permission and **0** to revoke them

## Permissions

| Permission  | Description |
| ------------- | ------------- |
| CommandRate  | Allows you to use the !rate command |
| CommandFeature | Allows you to use the !feature command|
| CommandEpic | Allows you to use the !epic command|
| Commandunepic | Allows you to use the !unepic command|
| CommandVerifycoins | Allows you to use the !verifycoins command|
| CommandDaily | Allows you to use the !daily command|
| CommandWeekly | Allows you to use the !weekly command|
| CommandDelete | Allows you to use the !delete command which deletes levels|
| CommandSetacc | Allows you to use the !setacc command which lets you set the account who made the level|
| CommandRenameOwn | Allows you to use the !rename command on thier **own** levels|
| CommandRenameAll | Allows you to use the !rename command on **all** levels|
| CommandPassOwn | Allows you to use the !pass command which lets you change passwords on **your** own levels only|
| CommandPassAll | Allows you to use the !pass command on **all** levels|
| Commanddescriptionown | Allows you to use the !description command on your **own** levels|
| Commanddescriptionall| Allows you to use the !description command on **all** levels|
| CommandPublicOwn | Allows you to use the !public command on your **own** levels|
| CommandPublicAll | Allows you to use the !public command on **all** levels|
| CommandUnlistOwn | Allows you to use the !unlist command on your **own** levels|
| CommandUnlistAll | Allows you to use the !unlist command on **all** levels|















