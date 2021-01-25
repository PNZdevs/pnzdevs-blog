---
title: PHP Parse error - syntax error, unexpected '?'
metaDescription: solution to PHP Parse error - syntax error unexpected '?'
date: 2021-01-02
author: Mattia Penna
---

## PHP doesn't recognize question marks

Ever seen this error on your console while developing on your *Laravel* project? On your *wordpress* site? Or maybe on your *xampp?* 

<!--more-->

If you are reading this, odds are that you are getting this error in your ```vendor``` folder.

Well don't worry, it's no big deal or any kind of complicated error. Chances are that **your php in not up to date!**

## What are the ? before variables type in PHP

Those '?' that gives you error ara a syntax called **Nullable Types** in php and have been implemented in PHP 7.1.

*Nullable type simply means when you prepends ? to the type name while declaring types in the method parameters or for return values, it will be marked as nullable. This signifies that as well as the specified type, NULL can be passed as an argument, or returned as a value, respectively.* More info [on PHP oficial page](https://www.php.net/manual/en/migration71.new-features.php)

So, if you type hint parameter with ? like below:
<br><br>

```php
function printMe(?string $name)
{
  var_dump($name);
}

printMe('FooBar'); // string(10) "FooBar"
printMe(null); // NULL
```

As you can see, the method will accept both string and null as a parameter without any error and process them likewise. But if you don’t pass any arguments it then it will result into a fatal error.

So there you have it, if you want to use those dependencies **you have to update your PHP to at least version 7.1!**