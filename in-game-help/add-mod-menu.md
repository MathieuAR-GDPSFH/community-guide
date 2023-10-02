---
description: This guide will teach you how to add a Mod Menu to your GDPS on mobile and PC.
---

# Adding a Mod Menu to your GDPS

(This page may need a rework in the future, some information is lacking)

## Mobile (Android)

To add a mod menu to your GDPS you must have the following.

* A Hex Editor (Required for method 1)
* Italian Apk Downloader's Mod Menu - [Download it here](https://www.youtube.com/watch?v=YNF\_wk7uMuA)
* APK Editor
* Base64 Encoder [Website Link](https://www.base64encode.org/) (Required for method 1)
* Your GDPS' APK

### Method 1 (Manual Replacement; Complicated)

1. Open APK Editor
2. Tap "Select an APK File"
3. Find the APK of the **Mod Menu** - Not your GDPS or the original game!
4. Tap "Simple Edit"
5. Navigate into the folders as seen on the images below "lib" / "armebi-v7a" 

&#x20;![](../.gitbook/assets/Screenshot\_20230923-121906-751.png) ![](../.gitbook/assets/Screenshot\_20230923-121920-007.png)

6. Save "libcocos2dcpp.so"

&#x20;![](../.gitbook/assets/Screenshot\_20230923-121944-133.png)

7. Open your Hex Editor
8. Find "libcocos2dcpp.so" you have extracted from the Mod Menu APK and open it
9. Search for "www.boomlings.com/database". Make sure to look for "String" rather than "Hex".

&#x20;![](../.gitbook/assets/Screenshot\_20230923-122017-727.png)

10. Tap on "Find and Replace" and replace "http://www.boomlings.com/database" with your GDPS link. Make sure your GDPS link is the exact same length as the original link as shown in the image below

If it is not the same length, you may do the following depending on if its too long or too short

If its too long, you may delete the https:// from the link to make it the same length.

If its too short, you can add slashes to it.

Check the below image for examples:

![](<../.gitbook/assets/image (1).png>) <- Tap on the image to zoom in.

11. Open the [Base64 Encoder](https://www.base64encode.org) and type "http://www.boomlings.com/database" and press "encode"
12. Copy the result and search for it in your Hex Editor
13. Go back to the [Base64 Encoder](https://www.base64encode.org) and type your GDPS link into the box and press "encode" (same length-specific rule applies as in Step 10.)
14. Copy the result and find and replace the Base64-encoded boomlings link with your Base64-encoded GDPS link.
15. Save the file
16. Open APK Editor
17. Tap on the APK of the **Mod Menu**
18. Tap "Simple Edit" and navigate back to the "lib" / "armebi-v7a" folder.
19. Replace the "libcocos2dcpp.so" with the modified one you created ![](../.gitbook/assets/Screenshot\_20230923-122109-054.png)
20. Save the APK.

### Method 2 (Transfer existing libcocos2dcpp.so file from your GDPS APK)

1. Go into APK Editor and select your GDPS' APK file instead
2. Tap on "Simple Edit"
3. Navigate to "lib" / "armebi-v7a"
4. Find "libcocos2dcpp.so" and save it
5. Go back and select your **Mod Menu** APK
6. Navigate to the "lib" / "armebi-v7a" (again)
7. Replace the old "libcocos2dcpp.so" with the one from your GDPS
8. Save the APK.

Your GDPS should now bave the mod menu in it when you open it!

### Optional Steps
Optionally you can replace the package name to separate your GDPS with the original game.

1. Open APK Editor
2. Find the APK in the "ApkEditor/tmp" folder
3. Tap on "Common Edit"
4. Change the App icon/name or whatever you would like
5. Change the package name to whatever you like. Please do **not** put numbers at the start of the package name.

The APK should now work whilst being separate from the original game. If you encounter an issue with installing it, [check here on how to fix "damaged" packages](../faq/package-parsing-error-android.md).

## PC (Windows)

### GDMegaOverlay

This part of the guide will teach you how to add GDMegaOverlay to your GDPS, GDMegaOverlay us a free alternative to Mega Hack v7 and includes most of MegaHack v7's features

1. Open your GDPS folder you have extracted (The folder you get when downloading your GDPS from the GDPSFN Panel)
2. Download the "gdmo" folder from the [GDMegaOverlay GitHub page](https://github.com/maxnut/GDMegaOverlay) and extract it
3. Copy all the files over to your GDPS' folder. If you're prompted to replace files, click on "yes".
4. Load up your GDPS and press "tab" if the mod menu appears, you've installed it properly!

### Mega Hack v5

You can't really "install" Mega Hack to a GDPS. But you can still bind it to your GDPS.

You will need to download a hex-editor like [HxD](https://mh-nexus.de/en/downloads.php?product=0).

1. Download and extract Mega Hack v5
2. Open MegaHack.exe in HxD
3. Search and Replace (CTRL+R) for "GeometryDash.exe" with your GDPS' exe name. Make sure that your GDPS' .exe name has the exact same length as GeometryDash.exe.\
   If the length doesn't match, backup your GDPS account and rename your GDPS' .exe name to something fitting.\
   <mark style="color:red;">If HxD prompts "This replace operation changes the file size", do NOT proceed.</mark>
