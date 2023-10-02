---
description: Assign special permissions to moderators using PHPMyAdmin
---

# Assigning special Moderator functionality

## Special moderators permissions

Many people do not know about this section but it is useful for moderators.

### modipperms table structure

| Name           | Information                                | Args                                              |
| -------------- | ------------------------------------------ | ------------------------------------------------- |
| categoryID     | Add a unique number to the category        | (optional)                                        |
| actionFreeCopy | Permission to obtain free copies of levels | (Disabled by default) \[0: Disabled / 1: Enabled] |

### Creating a category

Learn to access phpMyAdmin: 🔐 [Accessing to phpMyAdmin](site-structure.md)

Learn phpMyAdmin structure: 🔐 [Site Structure](site-structure.md)

1. Access to your phpMyAdmin database and Look for "modipperms".
2. Open the insert tab.
3. Fill out all fields correctly.
4. Click on "Go".
5. You have created special mod permission correctly!
