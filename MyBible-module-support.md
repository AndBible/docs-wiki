## Experimental MyBible module support

Starting from `4.0.639` there is an experimental module support for MyBible module format, more specifically for Bible and Commentary modules.

1. Connect your device to computer with USB cable. 
2. Create a new folder `Android/data/net.bible.android.activity/files/mybible` 
3. Copy MyBible module files there. If you have MyBible installed, you can find its module files in `Android/data/ua.mybible/files/MyBible` (look for `*.SQLite3` files).
4. Restart And Bible and you will find the modules now installed.


## Custom add-on modules that provide MyBible documents for And Bible 4.0.640+

And Bible 4.0.640+ supports offering new fonts to users with custom addons modules.

Define category as "And Bible" and your fonts with AndBibleProvidesMyBibleModules keys, like in the following example:

```
[MyBibleExample]
DataPath=./modules/texts/ztext/MyBibleExample/
Version=1.0
ShortPromo=Provides example MyBible module (FiAapeli; Aapeli Saarisalo UT 1969)
Description=Provides example MyBible module
DistributionLicense=Public Domain
Category=And Bible
ModDrv=RawGenBook
InstallSize=1331668
AndBibleMinimumVersion=640
AndBibleProvidesMyBibleModule=FiAapeli;FIASUTa.SQLite3
```

Put your MyBible module files (here `FIASUTa.SQLite3`) in your module folder, i.e. to 
`./modules/texts/ztext/MyBibleExample/`.

`AndBibleMinimumVersion` refers to build number (the last three digits in the version, i.e 4.0.640).

See examples: https://github.com/AndBible/special-modules/

### Please note that this is unsupported and experimental feature. It might or might not work. Use at your own risk!