# And Bible FAQ #

## I can't find ESV any more in Downloads. What's wrong?

The publishers of the ESV have unfortunately decided it is not longer in their interest to publish towards SWORD platform (by Crosswire Bible Society) which And Bible is using.

We are in progress in investigating options to bring ESV back to And Bible. See [#390](https://github.com/AndBible/and-bible/issues/390).

If you still have ESV on your other device, you can get ESV from your old device by backuping module and
restoring on new device. Please see https://youtu.be/2zcme61EajQ how to do it via "backup modules" feature.
This applies to And Bible 3.3 and later.

## Please add module X to And Bible!

Modules to And Bible are provided via JSword engine, which uses Sword modules by Crosswire and couple
of other freely available module repositories. Thus, you should primarily make your requests to Crosswire modules team.

You can also get in touch with them via email to their [email list](https://www.crosswire.org/mailman/listinfo/sword-devel) or via their other [contact methods](http://crosswire.org/contact/). See also their [FAQ](https://wiki.crosswire.org/EnduserFAQ) and their [
Instructions how to contact copyright holders](https://wiki.crosswire.org/Copyright).

If the text is not copyrighted (i.e. it is public domain), there could be a shortcut to get it quickly to 
And Bible. In that case, please contact us. 

## I found text issue in one of the Bible / Commentary etc. modules in And Bible. 

And Bible developers don't fix module issues. Modules to And Bible are provided primarily
via JSword engine, which uses Sword modules by Crosswire. Thus, you should report your problem 
to Crosswire modules team.

You can report module issues directly via their [issue tracker](https://tracker.crosswire.org/projects/MOD/)

You can also get in touch with them via email to their [email list](https://www.crosswire.org/mailman/listinfo/sword-devel) or via their other [contact methods](http://crosswire.org/contact/).


## I have older phone, that doesn't have Android 4.4+. Can I use And Bible?

Yes, you can download old, unsupported version from [here](https://github.com/AndBible/and-bible/releases/tag/build-02.09.05).

## Is there any way to change the voice of the speech synthesis in And Bible?

How voice is changed varies between different TTS engines. 

If you are using Google Text To Speech Engine in particular (which you can also install from [here](https://play.google.com/store/apps/details?id=com.google.android.tts)),  you can change the used speech voice as follows: System TTS settings -> Settings icon button -> "Install voice data" -> "English (United States)" -> voice selection appears.

## Is there version for iOS (Apple iPhone / iPad) in plans?

No, unfortunately this app is exclusively for Android at the moment, and there are no 
plans to make it for iPhone, as long as there are no easy paths of porting native Android
apps to iOS.

For iPhone, there is another sword-based app, called PocketSword, that you might want to try. 

## I have downloaded one bible but how do I download more bibles, commentaries etc. ##

To download bibles, commentaries, and books start And Bible and select Menu button (see 'Where is the Menu Button' below) / More / Download Documents.

Downloads are best done when connected via WiFi but you can download using your normal mobile data connection.

## Where is the Menu button ##

The Menu button is not always clearly visible on some recent phones.  Sometimes it is represented by 4 horizontal lines or 3 vertical dots.  Recent HTC devices may have a stripe along the bottom of the screen containing only 3 dots, or you may need to long-press the App-switcher or Home button.  The Acer Z3 requires that you double tap the multitask button.

## How do I copy My Notes and Bookmarks to my new phone ##

This is done by backing up on one phone and restoring on the other.
  * On the old phone select Menu/More/Backup/Backup
  * Note the backup directory location in the confirmation message
  * Either copy the backup folder to the new phone or move the SD card.
  * On the new phone select Menu/More/Backup/Restore

If one device has an internal and external SD card the location of the backup folder may not be on the removable SD card but can still be copied via USB cable.

The backup created by And Bible is a SqLite database file named andBibleDatabase.db stored in a folder named andbible\_backup on your SD card or, with some devices, the primary internal storage.

You may wish to copy this file to your pc via usb after backup to ensure you do not lose any data.

If you are having difficulty restoring i) ensure you have a copy of your backup file ii) do a backup and observe the location of the new andBibleDatabase.db iii) overwrite the 

## Where is the exit button?

You can exit the application like any other android application by going to home screen (via home button). 
Android memory management might stop the application if it needs memory for other apps. In normal Android applications
there is (and should not) be a specific exit button.

## Where do the Bible translations for And Bible come from?

All documents available in And Bible are either in the public domain or are licensed such that they are permitted for distribution. You can see a full list of them at these sites:
* https://crosswire.org
* https://ibtrussia.org
* https://ebible.org
* https://public.modules.stepbible.org
* https://andbible.github.io

## How do I downgrade from 4.0 to 3.3?

Go to Main menu > Backup & Restore

1. From under 'Import & Export', select an earlier backup to be exported (it is preserved for 1 month). 
2. Back up file called `dbBackup-33-*.db` (where * is timestamp) somewhere. 
3. You might want to back up also modules, from the same screen.
4. Then uninstall app. 
5. Then install 3.3 from [Github Releases page](https://github.com/AndBible/and-bible/releases/tag/production-400). This will probably prompt you to allow installs from Unknown Sources. Change the setting so you can install v3.3.
6. Then from Main Menu > Backup & Restore, restore the backup file that you just exported from v4.
7. To make sure, And Bible does not get upgraded automatically, you might need check your auto-update settings in Google Play (or in any other App store you that are using that provides And Bible). 