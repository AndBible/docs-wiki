# And Bible FAQ #

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

If you are having difficulty restoring i) ensure you have a copy of your backup file ii) do a backup and observe the location of the new andBibleDatabase.db iii) overwrite the new file with the old backup file iv) do a restore.

## Can I manually add modules/documents to And Bible? ##

Yes, you can copy modules to a jsword directory on your sd card.  Expand the module so that the .conf file is in sdcard/jsword/mods.d and the bible files in a subdirectory of sdcard/jsword/modules e.g. sdcard\jsword\modules\texts\ztext\nettext.

The main source for modules to manually install is: http://www.crosswire.org/sword/modules/index.jsp or http://www.crosswire.org/ftpmirror/pub/sword/raw/.

There is a list of module repositories here: http://www.crosswire.org/wiki/Module_Repositories

Modules/documents installed via the Download screen in And Bible will be placed in a different directory.

## Why are Bible books listed vertically in the portrait mode passage selector ##

Listing books vertically when in portrait mode allows longer sequences of books and therefore makes it easier to locate the correct column for the book you are seeking.

This is in some ways similar to the list of books at the front of bibles which normally run vertically in 2 or 3 columns.

In the future I plan to add a vertical line separator between OT and NT books to guide user's eyes.

Landscape mode Bible books are listed horizontally for the same reason as above.

## Can I delete a document from And Bible ##

To delete a document:
  * display the documents list
  * long-press on the document
  * select Delete

This will also delete the document's index.

Documents currently being displayed cannot be deleted, and neither can documents that have only just been downloaded.

## How can I get help? ##

The [And Bible Discussion Group](https://groups.google.com/group/and-bible) allows you to ask questions or discuss And Bible features.

Alternatively e-mail help.andbible@gmail.com

## Psalms in French Bibles are Offset by One ##
This is due to the unusual versification used by the Sword modules containing French Bibles like FreSegond and FreCrampon.

Please see [this discussion](http://www.crosswire.org/pipermail/sword-devel/2014-March/041180.html) on the sword-devel mailing list.

## I want integration with Strong's Concordance ##

This has been implemented.  There are several bibles containing Strongs references, such as ESV2011 and KJV.

## How can I go to a Strong's Reference Number ##

You can go to a Strong's reference by
  * clicking a link in a bible containing Strong's references
  * when viewing Strong's select MENU/Contents and then enter the desired no e.g. 02227 - remember the initial zero.
  * swipe left/right when viewing a Strong's page to go to next/prev ref
Release 0.4.0 will allow a list of all occurrences of a Strong's number to be displayed.

## Can I generate my own indexes and manually copy them to my Android mobile ##

To allow for auto-uninstall of application generated files indexes are generated to the appropriate module sub-dir of /mnt/sdcard/Android/data/net.bible.android.activity/files/lucene/Sword e.g. ESV indexes are in ../lucene/Sword/ESV.

Sword generated indexes partially work in And Bible but fully compatible indexes must be generated using a recent JSword application on JDK 1.5+.

The best, quickest and most reliable method to get a search index is to download it using And Bible as requested the first time you request a Search.

## What are the permissions for? ##

And Bible requires the following permissions:

1. Full network access
    In order to download Bible versions
1. (optional) Modify or delete the contents of your SD card + read the contents of your SD card
    In order to backup / restore bookmarks
1. Read phone status and identity (only until Android 5 (Lollipop))
    In order to stop Speak if a call comes in