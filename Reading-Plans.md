# Reading Plan #

Reading plans are accessible via Menu/More/Reading Plan.

On first access you select a plan and are taken to the Daily Reading screen for the first day.

The Done button will be enabled after pressing Speak or Passage for each passage.  Done causes the Daily Reading to move to the next day and if you are behind will take you to the next day's readings.

## Custom Reading Plans ##
It is possible to create a custom reading plan for use with And Bible.

You will need to create a file similar to the examples [here](https://github.com/AndBible/and-bible/tree/master/app/src/main/assets/readingplan) which are the reading plans distributed with And Bible.  The name of the file will be the name of the plan.  The file extension must be .properties and you must place it on your mobile's sdcard in a folder named jsword/readingplan.  Use a simple text editor to create the file e.g. Notepad++ and do not use something like Word.  The file must contain a series of rows in the format day=reading1,reading2 E.g.
```
1=Gen.1, Matt.1
2=Gen.2, Matt.2
3=Gen.3, Matt.3
4=Ps.119
5=1Cor.1, Jude
```

It is possible to skip days e.g. if you do not wish to a reading at the weekend. E.g.
```
1=Gen.1, Matt.1
3=Gen.2, Matt.2
```

You can also add a date-based reading plan, which includes the month and day number for each day. The only difference of this type of plan from the regular plan, is that the date-based plan will always open at today's date by default. The regular plan opens the current day, which is the day up to where you are done reading. The file for a date-based plan must always begin the readings at `1=`. Also, the date must be in the format of 3 letters for the month, then dash and month day number followed by semicolon (;). E.g.
```
1=Jan-1;Gen.1-2,Ps.1-2,Matt.1-2
2=Jan-2;Gen.3-4,Ps.3-5,Matt.3-4
3=Jan-3;Gen.5-6,Ps.6-8,Matt.5
...
146=May-26;Jos 12,Isa 16,2Tim 2
...
334=Nov-30;Est 7-8,Oba,Heb 3-5
```

OSIS format references must be used and OSIS Bible book names must be used.  These will be translated to the current language when displayed in And Bible.  E.g. Gen.1,Matt.1-Matt.2,Ps.119.1-Ps.119.10

Example reading plans can be found [here](https://github.com/AndBible/and-bible/tree/master/app/src/main/assets/readingplan).

A full list of OSIS book names can be found [here](https://wiki.crosswire.org/OSIS_Book_Abbreviations)

##### Deuterocanonical Books #####
The default versification for reading plans is KJV.  If you wish to include deuterocanonical books  in your plan you must specify the versification in the properties file.  E.g.:
```
Versification=Vulg
1=Sir.1-Sir.2
2=1Macc.1-1Macc.2
3=Bar.1-Bar.2
```

## Set Start to Another Day ##
If you started the readings on a previous day and have just switched to And Bible then select Menu from the Daily Reading screen and then select 'Set Start Date...'.  You may then jump to 'Move the current day to a specific day' below to skip over readings you have already done.

## Abandon Reading Plan ##
Press Menu/Reset from the Daily Reading screen.

## Switch between Reading Plans ##
Select the first button in the toolbar when in the Daily Reading screen.  By this means it is possible to use several plans simultaneously.

## Preview a plans readings ##
When in the Daily Reading screen select the second button in the toolbar.

## Go to a specific day ##
When in the Daily Reading screen select the second button in the toolbar.  Then select the required day from the list.

## Move the current day to a specific day ##
This is useful if you have been using a reading plan externally from And Bible.  A sequence of actions might be i) select plan ii) Set start date to another day (as above) iii) Move the current day to a specific day (as below)

**Version 3.3 and earlier:** Go to the day prior to the desired day as described in the above paragraph.  Select Menu/Done (not the normal Done button at the bottom) this bypasses checks and marks the current day as Done and the next day will become the current day.

**Note:** Starting in 3.4-beta (and 3.4 stable), you will be able to simply go to 3-dot menu on top right, and click "Set as current day".