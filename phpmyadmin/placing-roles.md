---
description: >-
  Assign a user a role using PHPMyAdmin
---

# Placing a role using PHPMyAdmin

## Placing role structure

| Name | Information | Args |
| ---- | ----------- | ---- |
| assignID | Add a unique number to the assing | (optional) |
| roleID | [ID of the role](create-roles.md) you want to place | (from the "roles" table) |
| accountID | ID of the account user you want to place | (from the "accounts" table) |

## Placing a role to a user

Learn to access PHPMyAdmin: 🔐 [Accessing to phpMyAdmin](phpmyadmin/site-structure.md)

Learn PHPMyAdmin structure: 🔐 [Site Structure](phpmyadmin/site-structure.md)


1. Access to your PHPMyAdmin database and Look for "roleassign".
2. Open the insert tab.
3. Fill out all fields correctly.
4. Click on "Go".
5. You have assigned a role to a user!