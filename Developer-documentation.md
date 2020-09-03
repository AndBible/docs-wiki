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

### Run separate debug app on your device
It is possible to install And Bible as 2 different IDs on your device. This is really having 2 installs of And Bible on one device. To build the debug version as a separate app, simply open `local.properties` file (which is in the root of the development project), and add this line at the bottom: `APP_SUFFIX=.debug`

Now when you build the app it will create a separate And Bible application on your device. **Please note** that both icons and app titles look exactly the same, so you have to figure out which one is which.

## Running tests

Configuration for running tests in Android Studio:

![Test configuration in Android Studio](https://user-images.githubusercontent.com/5811789/48984311-c4df5780-f102-11e8-937b-c5d438b79629.png)

For running tests, you need to install test modules. There is one module in test modules package that we don't have permission to distribute publicly, so please contact us (and-bible-support@googlegroups.com) if you need to run tests. Travis CI does does have these modules.

## Contributing code

- Consider writing unit tests (whether it is very important or not depends on the type of code you write)
- Run tests and fix any that happen to be broken after your improvements
- Create pull request towards master branch

### Code style guide

- Do not write too long lines (120 characters should be your guide)
- Preferrably write new code in Kotlin (i.e. if you need to create new file, create Kotlin file) 
- If you are planning to work on stuff that involves touching a lot of Java files, please discuss with Tuomas first. We are gradually migrating Java files to Kotlin and that should probably be done first.

### Branch naming

Please name your branches in the following syntax: `<type>/#<issue-number>_<name>`, where

- `<type>` can be one of:
  - feature
  - bugfix
  - improve
  - docs
  - refactor
- `<issue-number>` is the Github issue number. Use it where applicable, e.g. docs or refactor might not have an issue.
- `<name>` is a short human-readable name of the feature, spaces replaced with underscores (_).  

Example: feature/#100_improve_layout

## Building new jsword.jar for And Bible
- See instructions at [jsword-tweaks](https://github.com/AndBible/jsword-tweaks) repository

## Release testing
 - Test fresh install
 - Test migrations

## Making a new release 

 - Test release (see Release testing)
 - About 1-2 weeks before, `tx push -s` and call for translators 
    - Write release notes on a ticket (see for example #474)
    - Write translator context ticket (see for example #472)
 - Increment major or minor version and release 'release candidate' (RC) in Play Store
 - Prepare introduction video (See #475 for example)
 - Check from f-droid if jsword or jsword-tweaks need an update
 - Update translations (tx pull --force --minimum-perc 75)
 - Update Play Store & F-Droid & website description texts if needed
 - Merge develop to current-stable
 - Create new release/ branch from current-stable
 - Update .github/workflows/config.properties file
 - Tag a release (vx.x.xxx) and release in Play Store
 - Tag a f-droid release (vx.x.xxx-fdroid) for new automatic f-droid build
 - Make a facebook post
