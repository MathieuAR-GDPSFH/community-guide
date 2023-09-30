# Removing the Anti-Cheat (Android)

Geometry Dash has a built-in anticheat that kicks you out when completing a level that is either:

* Rated above 10 stars (except Main Levels)
* Rated above 2 stars AND a "Tiny" or "Short" level

This guide teaches you on how to get rid of the anticheat.

You will need the following:

* A hex editor. [Android download (NMM)](https://play.google.com/store/apps/details?id=in.mfile)
* A working APK editor

1. Extract the libcocos2dcpp.so file
2. In your APK editor, select your GDPS' APK
3. Go to the following folder: lib/Armeabi-v7
4. Save the libcocos2dcpp.so file
5. Open libcocos2dcpp.so file in NMM
6. Select search/goto. Type in the following (hex offset, not dec): \`0\x215416\`
7. Now, where your hex editor shows using the "I", type in 00\
   (if you cant find the the offset, where the hex editor shows 215410, go to the 6th column and type 00).
8. Save the file, replace old libcocos2dcpp.so file with new one you just edited.

Now you have removed the anticheat that keeps kicking you out!

## Video Guide

{% embed url="https://www.youtube.com/watch?v=aWI9ZLuQvH8" %}
