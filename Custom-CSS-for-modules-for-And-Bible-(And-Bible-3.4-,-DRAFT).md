And Bible offers option to include custom CSS and fonts in module zip files.
Place your CSS file under module directory (or subdirectory), and define CSS file path in config file with
AndBibleCSS=path-to/yourcssfile.css

CSS file you need to format as follows:

Prefix everything with .sword-YOURMODULE class (where YOURMODULE is the module initials of your module).
For night mode, prefix everything with .night class.

If you have used <hi type="my-type"> tag in your module, you can define css for your tags with .hi-my-type class definitions.

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
.sword-HISB .hi-x-hisb {
    display: inline-block;
    vertical-align: top;
    border: 2px solid #CAA810;
    border-radius: 2px;
    padding:3px;  
    margin-left:1px;
    margin-right:2px;
    margin-top:0em;
    font-size: 0.8em;
    color: navy; 
    text-decoration: bold;
    line-height: 1.2;
}

.sword-HISB .hi-x-hsb-l {
     display: inline-block;
    vertical-align: top;
    border: 2px solid #CAA810;
    border-radius: 1px;
    margin-left:1px;
    margin-top:0em;
    font-size: 0.8em;
    color: navy; 
    text-decoration: bold;
   line-height: 1.2;
}

.sword-HISB .hi-x-hsb-i {
    display: inline-block;
    vertical-align: top;
    border: 2px solid #CAA810;
    border-radius: 1px;
    margin-left:1px;
    margin-top:0em;
    font-size: 0.8em;
    color: navy; 
    text-decoration: bold;
   line-height: 1.2;
}

.sword-HISB .strongs {
   color: red; 
   font-size: 0.7em;
   vertical-align: sub; 
}

.sword-HISB .hi-x-hsb-italic {
    color: #CAA810;
    font-size: 0.8em;
    vertical-align: sub;
    font-style: italic;
}

.sword-HISB .hi-x-hsb-bold {
    color: #EA721C;
    font-size: 0.8em;
    vertical-align: sub;
    font-weight: bold;
}

.sword-HISB .hi-x-mdash {
    color: #909800;
    font-size: 0.7em;
    vertical-align: sub;
    text-decoration: none;
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

.night .sword-HISB .hi-x-hisb {
    display: inline-block;
    vertical-align: text-top;
    border: 2px solid #a1a1a1;
    border-radius: 3px;
    margin-left:5px;
    color: yellow; 
}

.night .sword-HISB .hi-x-hsb-l {
    display: inline-block;
    vertical-align: text-top;
    border: 2px solid #a1a1a1;
    border-radius: 3px;
    margin-left:5px;
   color: yellow; 
} 

.night .sword-HISB .hi-x-hsb-i {
    display: inline-block;
    vertical-align: top;
    border: 2px solid #CAA810;
    border-radius: 1px;
    margin-left:1px;
    margin-top:0em;
    font-size: 0.8em;
    color: white; 
    text-decoration: bold;
   line-height: 1.2;
}

.night .sword-HISB .strongs {
   color: red; 
   font-size: 0.7em;
  vertical-align: sub; 
}

.night .sword-HISB .hi-x-hsb-italic {
    color: white; /*#CAA810;*/
    font-size: 0.8em;
    vertical-align: sub;
    font-style: italic;
}

.night .sword-HISB .hi-x-hsb-bold {
    color:   white; /*#EA721C;*/
    font-size: 0.8em;
    vertical-align: sub;
    font-weight: bold;
}

.night .sword-HISB .hi-x-mdash {
    color: white; /*#909800;*/
    font-size: 0.7em;
    vertical-align: sub;
    text-decoration: none;
}

```