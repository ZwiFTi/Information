# Functions in JavaScript

## Table of Contents

1. [Description](#description)
2. [Construction](#construction)
  1. [Function/Methods](#construction)
3. [Good to know](#pour)
4. [First class functions](#wcag)
5. [Calling](#calling)
  1. [Functions](#cFunction)
  2. [Properties](#cProperty)
6. [Access self](#access)

## Description


## Construction

// declares the sayHello function
function sayHello() {
  var message = "Hello!"
  return message; // returns value instead of printing it
}

// function returns "Hello!" and console.log prints the return value
console.log(sayHello());

## Good to know

1. Functions are first-class functions
2. A key difference between a function and an object is that functions can
    be called (i.e., invoked with ()), while regular objects cannot.
3.



## First class functions

In many ways, a function in JavaScript can be treated as a value. Returning it from a function, storing it in a variable, and even passing it in as an argument into another function is perfectly allowed!


Functions can:
1. Be stored in variables
2. Be returned from a function.
3. Be passed as arguments into another function.

We can access properties of functions (function.length or function.name)

### Be stored in variables

var catSays = function(max) {
  var catMessage = "";
  for (var i = 0; i < max; i++) {
    catMessage += "meow ";
  }
  return catMessage;
};


### Be returned from a function

Declaring:
```
function alertThenReturn() {
  alert('Message 1!');

  return function () {
    alert('Message 2!');
  };
}
```
Calling:
```
alertThenReturn()();

// alerts 'Message 1!' then alerts 'Message 2!'
```

### Be passed as arguments into another function (callback function)

 A function that is passed as an argument into another function is called a callback function.


 
