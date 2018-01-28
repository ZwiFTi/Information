# Objects in JavaScript

## Table of Contents

1. [Description](#description)
2. [Construction](#construction)
  1. [Function/Methods](#construction)
3. [Modify, add, delete](#pour)
4. [Passing objects into functions](#wcag)
5. [Calling](#calling)
  1. [Functions](#cFunction)
  2. [Properties](#cProperty)
6. [Access self](#access)

## 1.0 Description

In JavaScript, an object is an unordered collection of properties. Each property consists of a key/value pair, and can reference either a primitive (e.g., strings, numbers, booleans, etc.) or another object.

## 2.0 Construction

List of things to note about objects:

1. Keys are strings (and quotes are optional)
2. The object is given a variable name assigned to it
3. Objects are unordered collections
4. Key/value pairs
5. Curly braces {}
6. Data within objects are mutable
7. Literal notation is best to use
8. Can include properties that point to functions called methods


  ```
  // Using literal notation:

  const myObject = {};

  // Using the Object() constructor function:

  const myObject = new Object();
  ```

### 2.1 Method

```
{
  name: 'Andrew',
  sayHello: function () {
    console.log('Hi there!');
  }
}
```


## 3.0 Modify, add and remove properties

* Delete: `delete printer.mode;`
* Modify: New value with either dot notation or bracket notation
* Add: New key/value pair with dot notation or bracket notation

```
  Example of adding a function:
  developer.sayHello = function () {
    console.log('Hi there!');
  };
```


## 4.0 Passing objects into functions

Since objects in JavaScript are passed by reference, if we make changes to that reference, we're actually directly modifying the original object itself! This is quite different than if we pass in primitives to functions!

## 5.0 Making changes to a copy

Since objects are passed by reference, making changes to the copy has a direct effect on the original object as well. In both objects, the value of the property is changed.

## 6.0 Calling on functions and properties

### 6.1 Functions/Methods


```
developer.sayHello();
// 'Hi there!'

developer['sayHello']();
// 'Hi there!'
```



Anonymous:
```
const greeter = {
  greet: function() {
    console.log('Hello!');
  }
};
```
Named:
```
const greeter = {
  greet: function sayHello() {
    console.log('Hello!');
  }
};
```

### 6.2 Properties

## Access self

A value for this is set when a method is invoked on an object, and that value refers to that object. Since it is a reserved word, it should not be used as any variable name, function name, etc.

```
const triangle = {
  type: 'scalene',
  identify: function () {
    console.log(`This is a ${this.type} triangle.`);
  }
};
```

## Window object

The window object is provided by the browser and is not part of the JavaScript language or specification. Any global variable declarations (i.e., those that use var) or global function declarations are added as properties to this window object.

### Variables

Only declaring variables with the var keyword will add them to the window object. If you declare a variable outside of a function with either let or const, it will not be added as a property to the window object.

Warning: Never use global variables (Why: Tight coupling, Name collisions)

## Get the keys and values for an object

`Object.keys()` returns an array of a given object's own keys (property names).  
`Object.values()` returns an array of a given object's own values (property values).

## FOCUS

## SEMANTICS

## STYLING
