# jsmin_minify #

The PHP5 port of JSMin used in the [Minify](http://code.google.com/p/minify/) project. It's [Ryan Grove's PHP port](http://github.com/rgrove/jsmin-php) with some added features.

* Regex literals are more reliably recognized. E.g. `return /'/;` does not throw an error.
* Multiline comments beginning with `/*!` are preserved.
* IE conditional comments are preserved.
* Code is unmodified if it looks like it's been run through Google Closure Compiler.

## usage & tips ##

    $javascriptCode = JSMin::minify($javascriptCode);

* Like all minifiers, JSMin.php is slow. Cache its output!
* If you need something 25x faster try the [jsmin PHP extension](http://www.ypass.net/software/php_jsmin/). 
* If you're combining multiple scripts into one file, it's wise to join them with `"\\n;"`.
