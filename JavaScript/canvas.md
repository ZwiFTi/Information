# Canvas in JavaScript

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

A powerful API which you can use to edit, resize and otherwise change images, animations, and interactions.

## Construction

In your HTML file:

1. Create a canvas tag
`<canvas id="c" width="200" height="200"></canvas>`
  - Width and height is optional
  - Gives us the space to work with on the website

2. Access canvas from JavaScript code
  1. Grab canvas using this selector:
  `var c = document.querySelector("#c");`
  2. From the canvas, grab its context
  `var ctx = c.getContext("2d");`

3. Start calling methods on this context `ctx`to start drawing on our canvas.


## Coordinate system

0,0 is on the top left corner.

x numbers get bigger as you go towards right
y numbers get bigger as you go down
