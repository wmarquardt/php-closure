# PHP Library for the Google Closure Compiler

A PHP class for optimizing and serving JavaScript sources using Google's 
[Closure Compiler web service](http://code.google.com/closure/compiler/docs/gettingstarted_api.html).
The sources will be compiled on demand and cached locally for performance.

Example usage:

```php
include("libs/php-closure.php");

$c = new PhpClosure();
$c->add("my-app.js")
  ->add("popup.js")
  ->advancedMode()
  ->useClosureLibrary()
  ->cacheDir("/tmp/js-cache/")
  ->write();
```

This was put together pretty quickly for use on [my website](http://pupius.co.uk).  Patches and improvements welcome!
