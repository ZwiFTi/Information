# Functions in JavaScript

## Table of Contents

1. [Description](#description)
2. [Construction](#construction)
  1. [New object](#construction)
3. [Good to know](#pour)
4. [This](#wcag)
5. [Calling](#calling)
  1. [Functions](#cFunction)
  2. [Properties](#cProperty)
6. [Access self](#access)

## Description


## Construction
```
function SoftwareDeveloper(name) {
  this.favoriteLanguage = 'JavaScript';
  this.name = name;
  this.sayName = function () {
    console.log(`My name is ${this.name}!`);
  };
}
```
### New object

let developer = new SoftwareDeveloper();

## Good to know

1. starts with Capital letter and is CamelCase
2. uses new operator
3. Should not have an explicit return value
4.

## This

JavaScript provides three methods that allow us to set the value of this for a given function:

* call() invokes the function and has arguments passed in individually, separated by commas.
* apply() is similar to call(); it invokes the function just the same, but arguments are passed in as an array.
* bind() returns a new function with this bound to a specific object, allowing us to call it as a regular function.
