javascript-best-practices
========================

When we work with javascript we should follow some rules or practice. Here are some practices I am writing with my exp.

* don't use Global Variables in javascripts. A global variable developer can change from any functions. If a developer pick the same name in a function.
* Always use a local variables in side a function. Always use var keyword when creating a variable other wise that variable will becase a global variable.
* Never declare String, Boolean or Number as an object. If you defined a then as an object result will be slows down execution speed
 Examples:
  var x = "John";             
  var y = new String("John");
  (x === y) // is false because x is a string and y is an object. 

* Don't use new Object()in your code 
  * Use {} instead of new Object()
  * Use "" instead of new String()
  * Use 0 instead of new Number()
  * Use false instead of new Boolean()
  * Use [] instead of new Array()
  * Use /(:)/ instead of new RegExp()
  * Use function (){} instead of new function()
Examples: 
  var x1 = {};           // new object
  var x2 = "";           // new primitive string
  var x3 = 0;            // new primitive number
  var x4 = false;        // new primitive boolean
  var x5 = [];           // new array object
  var	x6 = /()/;         // new regexp object
  var x7 = function(){}; // new function object

* Done use eval function in your code. The eval() function is used to run text as code. In almost all cases, it should not be necessary to use it. Because it allows arbitrary code to be run, it also represents a security problem.
* ignore if conditions for undefined checked. like

Examples:
  function(a,b){
    if(b === undefined)
      y = 0;
  }
  
Always usee this:
  
  function(a,b){
    y = y || 0;
  }

* Beware that numbers can accidentally be converted to strings or NaN (Not a Number). JavaScript is loosely typed. A variable can contain different data types, and a variable can change its data type:

Examples:
  
  var a = "hello";
  a = 10;
When doing mathematical operations, JavaScript can convert numbers to strings:

  var x = 5 + 7;       // x.valueOf() is 12,  typeof x is a number
  var x = 5 + "7";     // x.valueOf() is 57,  typeof x is a string
  var x = "5" + 7;     // x.valueOf() is 57,  typeof x is a string
  var x = 5 - 7;       // x.valueOf() is -2,  typeof x is a number
  var x = 5 - "7";     // x.valueOf() is -2,  typeof x is a number
  var x = "5" - 7;     // x.valueOf() is -2,  typeof x is a number
  var x = 5 - "x";     // x.valueOf() is NaN, typeof x is a number
  
* always use "use strict" directive in your file or function for writing more secure code. this will do not allow you to create a variable without var keyword. you can not create variables with name 'eval', 'interface', etc.



Contribute
==========
Please help me to write javascript best practice. :)
