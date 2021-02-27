And Bible offers option to include custom CSS and fonts in module zip files.
Place your CSS file under module directory (or subdirectory), and define CSS file path in config file with
AndBibleCSS=path-to/yourcssfile.css

CSS file you need to format as follows:

Prefix everything with .sword-YOURMODULE class (where YOURMODULE is the module initials of your module).
For night mode, prefix everything with .night class.

If you have used <hi type="my-type"> tag in your module, you can define css for your tags with .hi-my-type class definitions.
