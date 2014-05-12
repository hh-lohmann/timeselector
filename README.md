# Timeselector

A simple jQuery plugin for time selection in form.

**Version with ```jQuery``` as namespace descriptor ("function name") instead of its alias / shortcut ```$```**
  * *Original version: https://github.com/nicolaszhao/timeselector*
  * *This version: 2014-05-08 hh.lohmann@yahoo.de*


## What's wrong with "$"?

*Once upon a time, long before anyone could think of Javascript or even jQuery, [there were lots of higher (and lower) programming languages using "$" as a prefix for variables and some other stuff](http://en.wikipedia.org/wiki/Dollar_sign#Programming_languages). Then, in the beginning of the year 2005, there came [Prototype.js](http://en.wikipedia.org/wiki/Prototype.js), using "$" as a short form for some curious mixture of DOM and Javascript syntax, which was so impressing to some folks that they invented a whole new kingdom which they named "jQuery", and it took not long time that large parts of the world nowaddays grow up in the stern belief that jQuery is the current version of Javascript (if someone remembered "Javascript" at all) and that "$" is the basic building block of any computer that mankind ever had invented and ever will invent ...*

OK, let's get feet back onto the ground: you will run into some trouble if you implement jQuery or other code with "$" as a function name mixed with some other languages / [libraries](http://learn.jquery.com/using-jquery-core/avoid-conflicts-other-libraries/) or especially in a PHP based framework. The very easy solution is to use jQuery's actual function name which is, yes, "jQuery".


