# Custom font modules for And Bible 4.0+ 

And Bible 4.0+ supports offering new fonts to users with custom addons modules.

Define category as "And Bible" and your fonts with AndBibleProvidesFont keys, like in the following example:

```
[HebrewFonts]
DataPath=./modules/texts/ztext/HebrewFonts/
Version=1.0
Description=Provides Hebrew fonts "Sileo TSR" and "SBL Hebrew" for And Bible
DistributionLicense=Free to distribute
Category=And Bible
ModDrv=RawGenBook
InstallSize=501314
AndBibleMinimumVersion=506
AndBibleProvidesFont=Sileo TSR;and-bible/SILEOTSR.ttf
AndBibleProvidesFont=SBL Hebrew;and-bible/SBL_Hbrw.ttf
```

Put your fonts in and-bible/ subfolder of your module folder, i.e. to 
`./modules/texts/ztext/HebrewFonts/and-bible`.

`AndBibleMinimumVersion` refers to build number (the last three digits in the version, i.e. 3.3.506 -> 506).

See examples: https://github.com/AndBible/special-modules/