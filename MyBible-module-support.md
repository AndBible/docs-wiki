## Experimental MyBible module support

Starting from `4.0.639` there is an experimental module support for MyBible module format, more specifically for Bible and Commentary modules.

1. Connect your device to computer with USB cable. 
2. Create a new folder `Android/data/net.bible.android.activity/files/mybible` 
3. Copy MyBible module files there. If you have MyBible installed, you can find its module files in `Android/data/ua.mybible/files/MyBible` (look for `*.SQLite3` files).
4. Restart And Bible and you will find the modules now installed.


## Modules that use MyBible backend instead of Sword (And Bible 4.0.640+)

Now it is possible to create modules that use MyBible style sqlite3 data.

To implement this, first create config file (here, `mods.d/FiAapeli.conf`):

```
[FiAapeli]
DataPath=./modules/texts/ztext/FiAapeli/
AndBibleMinimumVersion=640
ModDrv=MyBibleBible
CompressType=ZIP
BlockType=BOOK
Encoding=UTF-8
SourceType=OSIS
Lang=fi
LCSH=Bible.Finnish
MinimumVersion=1.6.1
Description=Aapeli Saarisalo UT 1969 viitteineen
Versification=KJV
```

put your MyBible module file (here `FIASUTa.SQLite3`) in your module folder to your module folder
with name `module.SQLite3`, i.e here: `./modules/texts/ztext/FiAapeli/module.SQLite3`.

`AndBibleMinimumVersion` refers to build number (the last three digits in the version, i.e 4.0.640).
`ModDrv` can be either `MyBibleBible` or `MyBibleCommentary`, depending on the type of the content.

Module example: https://github.com/AndBible/special-modules/tree/master/FiAapeli

### Please note that this is unsupported and experimental feature. It might or might not work. Use at your own risk!