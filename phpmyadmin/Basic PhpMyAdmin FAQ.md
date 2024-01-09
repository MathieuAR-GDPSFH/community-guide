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

Now lets move on to the search tab!

## Search tab

This tab allows you to search for a specific value that is in a specific column

![image](https://github.com/nojnis/community-guide/assets/128159902/1350910d-64bd-4cc3-bf29-983ceed379f9)

- For example, if you wanna see how many levels were uploaded in game version 2.1 (if your gdps was updated to 2.2) type in 21 and use operator =, the other operators such as > should be self explanatory if you know basic math. The other ones such as !=   allows you to search for something that is not equal to the value you inputted. Now if you want to know the rest of the operators and what they do, you can either research what they do or experiment to see.

Now lets move on to the insert tab!

## Insert tab

This tab allows you to insert data into the database with specific values under specific columns.

![image](https://github.com/nojnis/community-guide/assets/128159902/84564cd3-7525-4c15-a3e7-9d23d71ecf83)

- It isn't possible to create levels in pma as GD level code is basically random characters, but for a table like roleassign or roles then insert tab will work, just fill in certain values and you good to go.
So the insert tab isn't complicated like you would've thought.

Now lets move on to the export tab!

## Export tab

This tab allows you to export the database as a .sql file (or just a specific table(s))

![image](https://github.com/nojnis/community-guide/assets/128159902/96a75b8a-ad12-4729-acd7-9cea12d99ab0)

- There are certain buttons like custom, which will allow you to select a specifc table(s) or row(s) to export as a .sql file such as for a backup of your GDPS database in case anything happens.
- Minmal will just export all tables or export a number of tables or rows you want to export (there is less customizability with this option.)
- Template is an export template such as a template to export a specific amount of tables or something like that.
- Extra: If you use export by a certain table, it will export row(s) of that specific table, if you select your main database (by clicking database name text) and go to export tab, then you can export your entire database or specific tables

Now lets move on to the import tab!

## Import tab

- This tab is pretty simple: This is where you will import a .sql database file into your current server (can be exporting a database that adds more rows, tables, columns, indexes, etc. or importing a brand new database if your server has no database at the time)

![image](https://github.com/nojnis/community-guide/assets/128159902/a88c3038-1822-4baa-bd6d-1c34a90d77da)

- This image shows all the optionss in the import tab.

- For things like character set of the file, you won't need to change that unless your database has different character sets. (you can research more about these if you are interested)
- Foreign key checks can be enabled or disabled (don't diable it unless you want to, also if you wanna learn about what it actually means you should research more about it)
- Format is the file format you will be importing (SQL would be what you usually import but you can import other files)
- SQL compatibility mode isn't needed unless your sql file needs it (you should know if your sql file needs compatibility mode as it would either say it or you would know if you coded it yourself)
- Do not use auto_increment for zero values means it won't auto increment values (add 1 to the value every time a new row of that data type is added) so if the defualt value is 0 then it won't auto increment.

Import tab isn't extremely complicated either, as if you were importing a GDPS database into pma, you wouldn't need to change any settings as default values are fine.

Now lets move on to the operations tab!

## Operations tab

This is a more complex table that you wouldn't need to worry about using for a GDPS.

![image](https://github.com/nojnis/community-guide/assets/128159902/750705cd-d1a3-4c2c-96f4-40494686a211)

- In this tab we can move a table to a different database (if you have more than one)

- We can also rename a table, add comments about it and some more values like collation which you won't need to know unles you really want to.

- Lastly we can copy a table to another database, whcih we can choose between: only the table structure, the structure and data or data only

![image](https://github.com/nojnis/community-guide/assets/128159902/36a9da5b-4e09-400d-ba35-6e51f16ee8cb)

- We now have table maintenance which allow you to optimize tables, check tables, analyze tables and more.

This was basically the most complicated tab (and part) of using pma, which most people won't need to use unless they wanna do extra stuff.

Now lets move on to the tracking tab!

## Tracking tab

- This tab allows you to track future changes to the specific table.

![image](https://github.com/nojnis/community-guide/assets/128159902/3539199d-b124-40ff-85d3-eed95c5a0580)

- These values such as delete are simple: it'll track the table to see if data gets deleted and tell you, as for the rest, they are also simple to understand.

Now that this tab was simple, lets move on to the final pma tab!

## Triggers tab

- This tab is the other complicated tab in pma, as you can add a trigger, to run specific SQL code in the database if a specifc event happened in the database.

![image](https://github.com/nojnis/community-guide/assets/128159902/32de561c-e51e-4de8-9013-c35c21d72e3b)

- It isn't necessary to understand how to make pma triggers, but it can be nice to know how to if you want to do a specific thing in the database when something happened (example: When a level is updated you will run sql code after that)

So now that you know what different tabs in pma do and may know the more complicated tabs if you decided to learn how to use them.

Hope this helps you understand pma even more!

# Extra FAQ

## How can I see an account's password as my friend forgot their password?

- You can't see their password, but you can reset it by simply going to https://bcrypt.online/ and typing in a password for them to change after and replacing the password column with new hash (yes the random symbols is called password hash.)









 
