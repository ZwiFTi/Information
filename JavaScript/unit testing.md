# Linting in JavaScript

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

Key: Expectations
Library to use: Jasmine
How to organize information: it and describe

## it

`it` are for identifying specification, spec.
`it` is the color `green`
`it` defines the boundaries around a test
a `spec` is a container for a test, or a way to identify the exact feature we are testing.
a `spec` can have multiple tests, but each test must return true to pass.

if expectations within a spec returns true, then that spec passes.

## describe

used to identify a suite,
`suite`: a group of related specs (everything contained in this block, is related to ex. Player)

describe is there to better organize test. A level of indentation!



## How to write a test

1. Call expect
2. Add 'the actual', what we want to test
3. Tell which comparison method you want to use

- `except('the actual').comparison();`
- `expect(add(2, 5)).toBe(7);` returns true if pass.

## Red-green-refactor cycle

1. You write your tests first
2. They all fail (no code to make them pass)
3. You write the code to make them pass
4. Refactor code and add new features
