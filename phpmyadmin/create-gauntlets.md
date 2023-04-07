---
description: >-
  There isn't really a tools page to help you create a gauntlet,
  so this will guide you through creating a gauntlet via phpMyAdmin.
---

# Create gauntlets with phpMyAdmin

1. Open phpmyadmin & login
2. Select the database starting with "gdps_"
3. Look for "gauntlets"
4. Open the insert tab
5. Fill in these things:
    * ID: This is the gauntlet id (1: fire, 2: ice, 3: poison, ...)
    * level1-5: These are the level ids (note: they will not appear in the order you put them in gd, they will appear in difficulty order)
6. Click on "Go"

If you're confused, here's a video:

{% embed url="https://www.youtube.com/watch?v=iISmYc0F7es" %}
