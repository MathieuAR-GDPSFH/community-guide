---
description: Assign a user a role using phpMyAdmin
---

# Assigning roles to a player

## Placing role structure

| Name      | Information                                         | Args                        |
| --------- | --------------------------------------------------- | --------------------------- |
| assignID  | Add a unique number to the assing                   | (optional)                  |
| roleID    | [ID of the role](create-roles.md) you want to place | (from the "roles" table)    |
| accountID | ID of the account user you want to place            | (from the "accounts" table) |

## Placing a role to a user

Learn to access phpMyAdmin: 🔐 [Accessing to phpMyAdmin](site-structure.md)

Learn phpMyAdmin structure: 🔐 [Site Structure](site-structure.md)

1. Access to your phpMyAdmin database and Look for "roleassign".
2. Open the insert tab.
3. Fill out all fields correctly.
4. Click on "Go".
5. You have assigned a role to a user!

If the user has a moderator-badge (with the req permission enabled), they can navigate in-game to Settings -> "Help" -> "Req" to activate the moderator buttons on levels.
