---
description: >-
  Another Guide make by a nerd.
---
This Guide is gonna teach you how you can use older versions of Geometry Dash on your GDPS!

#Prerequisites
So for this guide you will need some programs. I Reccomend you work on a computer since its a bit harder on android.

- Cvolton's GD Archive
The first and most important part of this guide is [Cvolton's GD Archive](https://www.mediafire.com/folder/s75xiy2a8yb3c/GD_Archive) as it has every version of GD.

- Hex Editor
This is the second most important part of this guide as you cannot do anything without it. I reccomend Using HxD on pc and For android i've really only used Hex Editor By first stack its really good! I'd advise you to turn off your Wi-Fi if you will use it as it has some ads that can get in the way.

- APK Editor
This is obviously needed for any version because you need to get it on android or else a majority of people cannot play on the gdps. This is optional if your on pc.

# GDPS' under 1.8
Since these versions are android only, its gonna be pretty simple.

## Method 1 (Use With APK Editor.)
Firstly, you need to open the APK in APK editor and pick "simple edit"
Second, we need to change the package name. So open up the "AndroidManifest.xml" and search for "com.robtopx.geometryjump" and then you can change it to your liking.

### Now its getting a little spicier!
We now need to "lib/armabi" and find the file called "libgame.so" which is gonna be the important information.
Now save it in a folder where you can find it and start editing the file using Our Hex Editor.

## Method 1, Hex Editing.
This is now the complex part.
- Step 1: Open up a base64 encoder, and type in "www.boomlongs.com" and encode it.
- Step 2: search for the encoded text in the hex code.
- Step 3: input your gdps site name. For example:
www.examplegdps.com
- step 4: Replace every instance of the encoded boomlings.com links with your new gdps links.
- Step 5: Replace it with the new one in APK editor and all should be good.

# GDPS' Over 1.8

Now its the PC era for gd and  