
The ``this`` variable inside functions
======================================

Functions **always** have a ``this`` variable, which is *implicit*.

* If you call a function without a "left object", ``this`` will be 
  [the global object](https://github.com/full-stack-bcn/samples/blob/master/javascript/functions/this/this-no-left-object.js), 
  or, in the browser, 
  [the window object](https://github.com/full-stack-bcn/samples/blob/master/javascript/functions/this/this-no-left-object-browser.html).

* If you call a function with a "left object", ``this`` 
  [will be that object](https://github.com/full-stack-bcn/samples/blob/master/javascript/functions/this/this-left-object.js).

So, all functions are methods, but if they are called without an object, the object will be the global object.


Constructors
------------

A function 
[can be used as a constructor](https://github.com/full-stack-bcn/samples/blob/master/javascript/functions/this/function-constructor.js)
by using the ``new`` operator, which creates a new object and binds it to the function ``this``.


Unbinding
---------

Even if we declare a method inside an object, it is an independent ``function`` object, so
[if we use it standalone](https://github.com/full-stack-bcn/samples/blob/master/javascript/functions/this/method-unbind.js) 
we loose the connection with its original object.

However, functions have a ``bind`` method which 
[sets the ``this`` variable](https://github.com/full-stack-bcn/samples/blob/master/javascript/functions/this/function-bind.js) 
inside the function. ``bind`` returns a *new* function which is bound permanently.