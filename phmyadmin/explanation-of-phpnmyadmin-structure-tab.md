# Structure tab of PhpMyAdmin
You may have noticed the structure tab at the top of the PhpMyAdmin website and wondered what it's for.
This guide will explain what this tab does and ways it can be used.
# Explanation of structure tab

Note: The structure tab is the same for all tables in PhpMyAdmin.
I will be using the levels table as an example.

## Extra information

If you see something like int(11) by type next to something like gameVersion, do not worry about changing this as this is default with your GDPS database.
 If you change it to varchar or anything different it could break your GDPS. 

# Structure tab function

The structure tab has multiple uses.

One use can be setting auto_increment value to 1 (So for levels levelID, you set auto_increment to 1 and now, level ID's will increase by 1 for every level uploaded.)
You can set the default value too. 
  It can either be a number, can be "none", it can be "NULL" (NULL means no value, 0.) and it can be undefined.

Comments: these are comments about a column in PhpMyAdmin, it will tell you what the column is for or any extra information about that column.
  (Doesn't always have a column.)

Extra: This tells you any extra functions of the column. An example is AUTO_INCREMENT.

Action: This allows you to edit the column, delete the column or change other values, such as making it primary.

# Examples of usage

There are tons of things you can do in the structure tab.

Here is an example: You can change "default" to 0 for likes or downloads or any other columns. (if default is "none" you might not want to change that.)

# What does stuff like int(11) mean?
- That stuff is the more complex side of PhpMyAdmin, you don't have to know exactly what they mean but if you want to, then you could research about all of it.
