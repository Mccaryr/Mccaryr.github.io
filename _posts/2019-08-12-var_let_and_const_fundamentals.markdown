---
layout: post
title:      "Var, Let, and Const Fundamentals"
date:       2019-08-12 12:41:25 -0400
permalink:  var_let_and_const_fundamentals
---


Declaring and assigning variables can be done in a few different ways with Javascript. The difference between var, let, and const is that var variables can be accessed anywhere within a function and let/const variables can only be accessed within the block they're initialized in. Hoisting is the default behavior of moving declarations to the top, in this respect only variables declared with var are hoisted and variables declared with let and const don't follow this rule. Using var, you could declare a variable after it has already been used, which is not the case with let and const (Using let or const would result in a referenceError). While this may seem like var is more flexible, it actually leads to more errors and bugs because Javascript only hoists declarations and not initializations (result would return undefined). This is a large reason why we use let/const instead, so Javascript can give us more verbose explanations for using variables outside of scope rather than just receive undefined we can get a referenceError on the variable in question. Scope can be defined as global,  function, and block scoped. It is the accessibility of variables throughout the program. Global scope means it would be able to be used anywhere and is assigned outside of a function and block. A major difference between var and let/const is that var is function scoped while let/const are block scoped. This means that in a block of code, using let/const, these variables only exist in that block and nowhere else.  Lastly, the major difference between let and const is that although both are block scoped, let can be reassigned a value while const must be....you guessed it, CONSTANT.  

```
//   An example of var hoisting

function hoist() {
console.log(message); 
var message = "Hoisting is sooo much fun!"; 
}

// The console would log undefined because JavaScript is executing line by line and isn't aware of the value of x. The //compiler views this code as....

function hoist() {
var message;
console.log(message)
message = "Hoisting is sooo much fun!";
}

// You can see that the declaration is "hoisted" to the top of the function but the initialization isn't. So to get this right we //need to declare and initialize the variable BEFORE we use it!

function hoist() {
var message = "Hoisting is sooo much fun!";
console.log(message)
}
```

```
// An example of differences in scope

function scopeTest(){
    if(true){
		                var color1 = 'red';
										let color2 = 'blue';
										const color3 = 'green';
										}
			console.log(color1);
			console.log(color2);
			console.log(color3);
			}
			
			scopeTest();
			
			//red
			// color2 is not defined
			//color3 is not defined
```
> Color 2 and 3 are undefined because they do not exist outside of their block scope, therefore we have a lot more control in their implementation.


