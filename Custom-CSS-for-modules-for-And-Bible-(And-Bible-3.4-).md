# DRAFT

And Bible offers option to include custom CSS and fonts in module zip files.
Place your CSS file under module directory (or subdirectory), and define CSS file path in config file with
`AndBibleCSS=path-to/yourcssfile.css`

CSS file you need to format as follows:

Prefix everything with `.sword-YOURMODULE` class (where `YOURMODULE` is the module initials of your module).
For night mode, prefix everything with .night class.

If you have used `<hi type="my-type">` tag in your module, you can define css for your tags with `.hi-my-type` class definitions.

Example:

mods.d/HISB.conf

```
[HISB]
DataPath=./modules/texts/ztext/HISB/
AndBibleCSS=style/style.css
...
```


Put your font file SILEOTSR.ttf to ./modules/texts/ztext/HISB/style/.
Define your css in ./modules/texts/ztext/HISB/style/style.css as follows

```
@font-face {
    font-family: 'Custom HISB Font';
    src: url('./SILEOTSR.ttf') format('truetype');
}

.sword-HISB {
    font-family: 'Custom HISB Font';
}

.sword-HISB .hi-x-trlit {
    color: green;
    font-size: 0.7em;
    vertical-align: top;
    font-weight: bold;
}

.night .sword-HISB {
    vertical-align: text-top;
 
    color: #00FF00; /*#green; */
}

.night .sword-HISB .hi-x-trlit {
    color:  white; /*#green;*/
    font-size: 0.7em;
    vertical-align: top;
    font-weight: bold;
}
```