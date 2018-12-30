# How to contribute code

## Building And Bible

1. Download and Install [Android Studio](http://developer.android.com/sdk).
2. Open a Terminal/command prompt.
3. Create a directory e.g. 'mydevdir' and change to that directory.

4. Run:
```
git clone https://github.com/AndBible/and-bible.git 
```

5. In Android Studio select File/Open.  Then open the and-bible folder with a green compass icon under mydevdir/and-bible/and-bible.

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

## Building new jsword.jar for And Bible
- See instructions at [jsword-tweaks](https://github.com/AndBible/jsword-tweaks) repository