# Remove 6-digit song ID limit (Android)

<mark style="color:purple;">(This page needs to be rewritten)</mark>

## How to remove 6 digit song ID limit from Android.

Don't you hate not being able to enter 7 digit song IDs without cheats? Well here is a guide that will tell you how to remove the limit. You will need: A hex editor. For PC, I recommend HXD for hex editing. For Android, i recommend NMM file explorer's built-in hex editor. An APK editor.

## Extract libcocos2dcpp.so file from APK.

Firstly in your apk, go to the folder: lib/Armeabi-v7 and save the libcocos2dcpp.so file.

## Open the libcocos2dcpp.so file

Using your hex editor, open the file. Now use goto/search and search for 322EBE (Hex offset not dec) Where the "I" indicates the offset is at, replace the 07 with 0C. Now save the libcocos2dcpp.so file.

## Replace the old libcocos2dcpp.so

Replace the old file with the new one and install.

Now you can enter 7 digit song IDs!
