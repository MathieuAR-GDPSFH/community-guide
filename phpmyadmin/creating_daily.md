---
description: >-
  Unfortunately, it's quite difficult to set today's daily level, so here's a step by step tutorial.
---

# Setting today's daily level

1. Open phpMyAdmin and login (GDPS Management -> GDPS Links -> phpMyAdmin).

2. Open the `gdps_{your gdps name}` database (it should be on the left side of the screen).

3. A lot of things will appear, and it may seem a little scary. Just find `dailyfeatures` and click on it.

4. At the top of the screen, you should see a taskbar. Find `Insert` and click on it.

5. Focus your attention on the `Value` column. Don't touch the `Function` column.

   ![image](https://github.com/xavwashere/community-guide/assets/97399129/bde9ef22-3a18-41df-8072-8b705ee26640)


7. The first option is `feaID`. This should be `1` if it's the first daily of your server, then `2` for the second, so on so forth. Don't press `ENTER` once you have entered it. Just click onto the next row.

8. Next is `levelID`. This should be pretty self-explanatory, but if not, just find the level ID of the level you want to set as daily and type it in. Again, don't press `ENTER`, just click onto the next row.

9. Now is where it gets a bit confusing. `timestamp` means the Unix timestamp that you want the daily level to appear on. You want this to be 12:00pm on the day that you want the daily to be on. To do this:
   
   8a) Open a new tab and go to https://www.unixtimestamp.com/ .
   
   8b) You should see this page, focus your attention to the red circle.
   
   ![image](https://github.com/xavwashere/community-guide/assets/97399129/bac3d1c9-e691-44d4-a697-d0d72a751c6d)
   
   8c) Now, set the year, month and day to the day that you want the daily to be on.
   
   8d) For hour set it to 0 and minutes to 0.
   
   8e) Set seconds to 1.
   
   8f) Now press convert. You should see a table. The number circled in the screenshot below is the number you will want to copy.
   
    ![image](https://github.com/xavwashere/community-guide/assets/97399129/6acc5b40-4447-49f1-99f5-69a67f6bd4dd)
   
   8g) Now go back to phpMyAdmin and paste the number into the timestamp box.

10. You don't need to worry about the `type` box. Now press the `Go` button that is underneath the area that you were typing.

11. Now your daily should be set! If you have any questions, don't hesitate to contact me on Discord: xavvvv.xd

12. You may want to set many dailies in advance. To do this, you can repeat this process while adding 1 to the previous `feaID` and setting the timestamp to the next day.
    
Thanks for reading! I hope you enjoyed!
