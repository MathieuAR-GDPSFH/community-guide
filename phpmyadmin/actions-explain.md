---
description: >-
  Explanation about the types of actions that you can find in the actions table in PHPMyAdmin
---

# Type of the table actions

Few people know what each **type of action** in this _specific table_ means, so here we will explain what each type means.

| Action Type | Information | Additional Args |
| ----------- | ----------- | --------------- |
| 2 | Appears when an account has been successfully logged in | **value1:** `UserName who logged`<br>**value2:** `IP of the user who successfully logged` |
| 3 | Appears when a level was liked (currently removed) | **value1**: `ItemID liked`<br>**value2:** `IP of user who liked`  |
| 4 | Appears when a comment was liked (currently removed) | **value1**: `ItemID liked`<br>**value2:** `IP of user who liked`  |
| 5 | Appears when an account comment was liked (currently removed) | **value1**: `ItemID liked`<br>**value2:** `IP of user who liked`  |
| 6 | Appears when a user has failed to log in to an account. If the user fails more than 6 times, they will not be able to try again for an hour. (account is disabled alert is displayed in-game) | **value:** `Account ID requested`<br>**value2:** `IP of user who failed login` |
| 8 | It means that a level has been removed | **value:** `Level deleted ID`<br>**value2:** `IP of the user who deleted the level` |
| 9 | Appears when a user has updated their in-game stats | **value:** `stars amount collected`<br>**account:** `User ID of the user updated stats`<br>**value2:** `stars coins amount collected`<br>**value3:** `demons amount collected`<br>**value4:** `usercoins amount collected`<br>**value5:** `diamonds amount collected`<br>**value6:** `moons amount collected` |
| 16 |  Used for GJP verifications of an account and updated every 1 hour, only appears if `sessionGrants` is enabled via `config/security.php` | **value:** `Account ID verified`<br>**value2:** `IP of the who has been verified GJP` |


## Trivia

- Many of the actions have been moved to their own sections and many types of removed actions (cvolton core) have not yet been found.
