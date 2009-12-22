# jsmin_minify #

The PHP5 port of JSMin used in the [Minify](http://code.google.com/p/minify/) project. It's [Ryan Grove's PHP port](http://github.com/rgrove/jsmin-php) with some added features.

* Regex literals are more reliably recognized. E.g. `return /'/;` does not throw an error.
* Multiline comments beginning with `/*!` are preserved.
* IE conditional comments are preserved.

### todo ###

* Add [fix](http://github.com/rgrove/jsmin-php/commit/f89f32db50e943515c7361ebcfb6a2cacf7dc91a) for systems using overloaded mbstring functions.
* Add unit tests from Minify