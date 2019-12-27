# How to contribute code

## Building And Bible

1. Download and Install [Android Studio](http://developer.android.com/sdk).
2. Install node.js from [http://nodejs.org/](http://nodejs.org/).
3. Open a Terminal/command prompt.
4. Create a directory e.g. 'mydevdir' and change to that directory.

5. Run:
```
git clone https://github.com/AndBible/and-bible.git 
```

6. In Android Studio select File/Open.  Then open the and-bible folder with a green compass icon under mydevdir/and-bible/and-bible.

While running And Bible in emulator, I'm using the following configuration:

![Selection_014](https://user-images.githubusercontent.com/5811789/56358437-42595080-61e7-11e9-98a5-4cf5903049c3.png)

## Running tests

Configuration for running tests in Android Studio:

![Test configuration in Android Studio](https://user-images.githubusercontent.com/5811789/48984311-c4df5780-f102-11e8-937b-c5d438b79629.png)

## Contributing code

- Consider writing unit tests (whether it is very important or not depends on the type of code you write)
- Run tests and fix any that happen to be broken after your improvements
- Create pull request towards master branch

### Code style guide

- Do not write too long lines (120 characters should be your guide)
- Preferrably write new code in Kotlin (i.e. if you need to create new file, create Kotlin file) 

### Branch naming

Please name your branches in the following syntax: `<type>/#<issue-number>_<name>`, where

- `<type>` is either feature or bugfix. Could also be refactor or improvement if it is clearly not a new feature or a bugfix. 
- `<issue-number>` is Github issue number
- `<name>` is short human-readable name of the feature, spaces replaced with underscores (_).  

Example: feature/#100_improve_layout

## Building new jsword.jar for And Bible
- See instructions at [jsword-tweaks](https://github.com/AndBible/jsword-tweaks) repository

## Making a new release 
 
 - About 1-2 weeks before, `tx push -s` and call for translators 
    - Write release notes on a ticket (see for example #474)
    - Write translator context ticket (see for example #472)
 - Increment major or minor version and release 'release candidate' (RC) in Play Store
 - Prepare introduction video (See #475 for example)
 - Check from f-droid if jsword or jsword-tweaks need an update
 - Update Play Store & F-Droid & website description texts if needed
 - Tag a release (vx.x.xxx) and release in Play Store
 - Tag a f-droid release (vx.x.xxx-fdroid) for new automatic f-droid build
 - Make a facebook post
