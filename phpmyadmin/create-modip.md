---
description: >-
  Assign special permissions to moderators using PHPMyAdmin
---

# Special moderators permissions

Many people do not know about this section but it is useful for moderators.

## modipperms table structure

- **categoryID:** Add a unique number to the category (optional)
- **actionFreeCopy:** Permission to obtain free copies of levels (Disabled by default) [0: Disabled / 1: Enabled]


## Creating a category

1. Open phpMyAdmin & login.
2. Select the database starting with "gdps_".
3. Look for "modipperms".
4. Open the insert tab.
5. Fill out all fields correctly.
6. Click on "Go".
7. You have created special mod permission correctly!

## Set special moderator permission to a role

1. Open phpMyAdmin & login.
2. Select the database starting with "gdps_".
3. Look for ["roles"](create-roles.md).
4. Create a new role or edit an existing role.
5. In the "modipCategory" field, enter the ID of the category.
6. Click on "Go".
7. You have assigned a category permission to a role!