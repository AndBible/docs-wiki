# Obsolete after And Bible 3.4

# Using a Custom Stylesheet to Change the Look or Layout of And Bible #

It is possible to change the colour, layout, or style of document text by creating a custom stylesheet.

# Details #

Create a css stylesheet using classes and attributes as found in these standard stylesheets: [style.css](https://github.com/mjdenham/and-bible/blob/master/AndBible/assets/web/style.css) [night\_mode.css](https://github.com/mjdenham/and-bible/blob/master/AndBible/assets/web/night_mode.css).

Name the files style.css or night\_mode.css and place them in a folder named 'jsword/css' on your sdcard.

The style.css file will always be loaded but the night\_mode.css will only be loaded when Night mode is selected.

The custom stylesheets will be loaded in addition the default And Bible stylesheets so it is only necessary to add the styles you wish to override.

After changing either css file And Bible will need to be restarted to show the changes.

## Example: Green Text in Night Mode ##
An example custom css file using green text for night mode follows.  To use this save it in jsword/css/night\_mode.css on your SD card or internal drive depending on your device.
```
/* make foreground text green */
body {
	color: #007000;
}

/* also make the headings green */
h1, .heading1 {
	color: #007000;
}
h1 a, .heading2, .heading3, .heading4 {
	color: #007000;
}
/* make cross references green */
a {
	color: #007000;
}
/* use a more browny colour for redletter otherwise it is too bright */
.redLetter {
	color: #3D1E06;
}
/* make the verse numbers green too */
.verseNo {
	color: #007000;
}
/* change Strongs to blue so as not to clash */
.strongs {
	color: #210C7D;
}
```
## Example: Override Default max-width ##
In release [2.10.0](https://github.com/mjdenham/and-bible/releases/tag/build-02.10.00), a change was made to the default style sheet that sets the maximum width of the text to 15cm, regardless of the width of the display. This may not be a desired outcome in some use cases, e.g., in landscape mode on tablets, so here's a simple custom style to override that change. To use this, save it in jsword/css/style.css on your sdcard.
```
body {
	max-width: 100%;
}
```
## Hi tag ##
In addition to the standard style classes used by And Bible module developers requiring a custom span tag may use the type `'x-*'`.
E.g.
```
<hi type='x-anything'>module text</hi> 
```
will result in:
```
<span class='hi hi_x-anything'>text</span>
```
So you may add the class 'hi\_x-anything' to your stylesheet.