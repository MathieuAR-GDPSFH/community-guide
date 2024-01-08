# What is PhpMyadmin?

- PhpMyAdmin is used for managing your GDPS database (or any database) and adding data, editing existing data and deleting existing data.

## How can I access PhpMyAdmin?

- You can follow this [community guide](faq/accessing-pma.md) <- This guide also explains its use a little better.

# I am confused by all the columns and indexes

- This is normal for anybody who hasn't made a GDPS before or used PMA(PhpMyAdmin) before.

Hopefully the next section can explain what all those columns and indexes do clearly enough for you.

# Explanation of the functions of the columns and indexes

- Firstly, to access the data of a pma table (so that it shows on the main pma page) click the text name of the table. (Note: Expand your gdps_(gdpsname) by clicking the "+" next to the name.)

- Now I will use an example of a table, in this example I use the levels table. (You might also be confused by the buttons at the top like structure, but we'll get to that later!)

  ![image](https://github.com/MathieuAR-GDPSFH/community-guide/assets/128159902/2247d5a9-6302-4743-9b3f-4f6412db54e2)

In this image you will see an example of what your levels table will have in it. (you may have more or less rows in it depending on how many levels you have in your GDPS.)

- So lets start with gameVersion, this should be self explanatory (kinda) where the number 21 would be 2.1, 22 2.2 and something like 18 being 1.8 as for binaryVersion this isnt self explanatory,
 but it is basically, the version code of the update (including bugfix updates), now for the other columns such as userName, this would be self explanatory. (If you want to know the exact functions of the rest of the columns, check out 
 [this in-depth explanation of the tables and columns](phpmyadmin/detailed-explanation-of-the-phpmyadmin-tables.md) which is very long.

Now lets move on to the structure tab!
## Structure tab
- Now here you may see certain things that are a bit more complex but I promise you, the complicated things like type and collation aren't necessary for a GDPS you don't plan on adding any custom code to.

 ![image](https://github.com/MathieuAR-GDPSFH/community-guide/assets/128159902/70eb5a06-8705-4d9d-8059-afd175cf2ce9)

 - Now I will tell you the columns you can ignore or do some extra research about these things. Ignore Type, Collation and Attributes as these aren't really necessary for using pma for just managing, editing and deleting data on the database.
- The column NULL means if the value is used or not, so if its yes, then that column isn't used. The next column, defualt either can have a value or can be none or NULL. usually the default value in the levels table, if there is one is 0 other tables maybe different.
- Comments are any extra information given about that column. Extra is any extra information, for levels table the level IDs are set to auto increment which means they will +1 to the number of the last ID of the last uploaded
- level, so if last level uploaded was ID 45, next will be 46 so IDs can be unique to every level.
- Note: DO NOT CLICK DROP FOR ANYTHING IN PMA AS IT WILL DELETE THAT COLUMN OR TABLE! (unless you are really sure about it, don't click it)
- under more, there are a few extra buttons such as unique, which will make that column unique but you can do extra research about that if you wanna know more.

- lastly at the bottom there are a few buttons

![image](https://github.com/MathieuAR-GDPSFH/community-guide/assets/128159902/7cdac95f-3e74-49ae-a773-3b7eba056e96)

for the buttons such as unique, you can research those if you wanna know what they do. just dont click drop on anything like I said before.
for all these buttons you can research more about them when you want to. (if you want)

Now lets move on to the SQL tab!

## SQL tab

This tab is pretty simple, you can run SQL code in this tab (don't paste random sql code in if someone told you to paste it in and run it!), but if you are running code, first click clear to remove existing filler text.

![image](https://github.com/MathieuAR-GDPSFH/community-guide/assets/128159902/e16eac63-f58b-46f8-a581-76649e27d6af)



 
