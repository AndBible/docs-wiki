## Users: MyBible module support (Experimental)

Starting from `4.0.640` there is an experimental module support for MyBible module format, more specifically for Bible, Commentary and Dictionary (starting from 4.0.641) modules.

1. Connect your device to computer with USB cable. 
2. Create a new folder `Android/data/net.bible.android.activity/files/mybible` 
3. Copy MyBible module files there. If you have MyBible installed, you can find its module files in `Android/data/ua.mybible/files/MyBible` (look for `*.SQLite3` files).
4. Restart And Bible and you will find the modules now installed.


## Module creators

It is now possible to create "Sword-like" modules that use MyBible backend instead of Sword (And Bible 4.0.640+).

### If you'd like to see some MyBible module distributed in And Bible, please  [suggest it here](https://github.com/AndBible/and-bible/issues/2122).

Now it is possible to create modules that use MyBible style sqlite3 data.

To implement this, first create config file (here, `mods.d/FiAapeli.conf`):

```
[FiAapeli]
DataPath=./modules/texts/MyBible/FiAapeli/
AndBibleMinimumVersion=640
ModDrv=MyBibleBible
CompressType=ZIP
BlockType=BOOK
Encoding=UTF-8
SourceType=OSIS
Lang=fi
LCSH=Bible.Finnish
Description=Aapeli Saarisalo UT 1969 viitteineen
Versification=KJV
```

put your MyBible module file (here `FIASUTa.SQLite3`) in your module folder to your module folder
with name `module.SQLite3`, i.e here: `./modules/texts/MyBible/FiAapeli/module.SQLite3`.

`AndBibleMinimumVersion` refers to build number (the last three digits in the version, i.e 4.0.640).
`ModDrv` can be either `MyBibleBible`, `MyBibleCommentary`, or `MyBibleDictionary` (support starting from 4.0.641) depending on the type of the content.

Module examples: [FiAapeli](https://github.com/AndBible/special-modules/tree/master/FiAapeli), [MyBibleStrongs](https://github.com/AndBible/special-modules/tree/master/MyBibleStrongs)

### Please note that this is unsupported and experimental feature. It might or might not work. Use at your own risk!