# How to remove The Anticheat from Android GDPS

It is very annoying being kicked out of a rated level 
thats above 30s and rated pver 2 stars.
This, is the guide everyone looks for.
You will need the following: 
A hex editor.
(For PC, I recommend HXD Hed editor, 
for Android, I recommend downloading NMM file explorer and using the built-in hex editor).
A working APK editor.
# Extract the libcocos2dcpp.so file
In your APK editor, go to the following folder:
lib/Armeabi-v7.
Save the libcocos2dcpp.so file.
--------------
# Open libcocos2dcpp.so file and follow these steps
After you open the file in your hex editor, select search/goto.
Now type in the following (hex offset not dec): 215416
Now, where your hex editor shows using the "I", type in 00
(if you cant find the the offset, where the hex editor shows 215410,
go to the 6th column and type 00).
Now save the file.
# Now just replace the old file with the new one
Replace old libcocos2dcpp.so file with new one you just edited.

Now you have remover the anticheat that keeps kicking you out!
