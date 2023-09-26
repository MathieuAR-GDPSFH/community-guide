---
description: >-
  Assign special permissions to moderators using PHPMyAdmin
---

# Special moderators permissions

Many people do not know about this section but it is useful for moderators.

## modipperms table structure

| Name | Information | Args |
| ---- | ----------- | ---- |
| categoryID | Add a unique number to the category | (optional) |
| actionFreeCopy | Permission to obtain free copies of levels | (Disabled by default) [0: Disabled / 1: Enabled] |


## Creating a category

Learn to access PHPMyAdmin: 🔐 [Accessing to phpMyAdmin](site-structure.md)

Learn PHPMyAdmin structure: 🔐 [Site Structure](site-structure.md)

1. Access to your PHPMyAdmin database and Look for "modipperms".
2. Open the insert tab.
3. Fill out all fields correctly.
4. Click on "Go".
5. You have created special mod permission correctly!

## Set special moderator permission to a role

<<<<<<< HEAD
Learn to access PHPMyAdmin: 🔐 [Accessing to phpMyAdmin](site-structure.md)

Learn PHPMyAdmin structure: 🔐 [Site Structure](site-structure.md)
=======
Learn to access PHPMyAdmin: 🔐 [Accessing to phpMyAdmin](phpmyadmin/site-structure.md)

Learn PHPMyAdmin structure: 🔐 [Site Structure](phpmyadmin/site-structure.md)
>>>>>>> f4e9a04d70d9f993f264a13568d636ada6c4831a

1. Access to your PHPMyAdmin database and Look for ["roles"](create-roles.md).
2. Create a new role or edit an existing role.
3. In the "modipCategory" field, enter the ID of the category.
4. Click on "Go".
5. You have assigned a category permission to a role!