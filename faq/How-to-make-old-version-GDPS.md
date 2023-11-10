# Resources needed
You will need:
A hex editor. (HxD for PC and NMM file explorer built-in hex editor/a hex editor you can find in the play store for Android)
Knownledge on logging into FTP.(There is a community guide about that.)
An older GD verson. [Cvolton Archive](https://www.mediafire.com/folder/s75xiy2a8yb3c/GD_Archive) to get all versions.
An APK editor.

# GDPS for 1.0 - 1.8
There are 2 methods for changing package name.
## Method 1:
Firstly, in your APK editor, click simple edit(If you are using an android APK editor, PC, click open contents.), edit the AndroidManifest.xml file using Notepad++ in this tutorial.
Click search, search in file, type in com.robtopx.geometryjump for the text you want to search for, and then make your own package name like: com.robtopy.gomeydumpdas (it must be the same length as original.)
Now click replace files and wait for it to replace. (replace in the unzipped APK contents.)
next, do the same thing like "com.robtopx.geometryjump" and replacing with "com.robtopy.gomeydumpdas", but this time, 
change com.robtopx.geometryjump to "Lcom/robtox/geometryjump" and replace with "Lcom/robtopy/gomeydumpdas"(Make sure to check match uppercase and lowercase letters.)
click replace files and wait until it replaces.

Now comes the more complex part. (Method 1) In the APK, go to the following directory: `lib/armeabi`. Save the libgame.so file somewhere.
Now, open it in your hex editor and do the following: click find and replace/search and replace, type in http://boomlings.com/database and replace with your server URL, example: https://badgpds.ps.fhgdps.com
click replace

