# JSON

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

JSON is a text-based data format following JavaScript object syntax. Many programming environments feature the ability to read (parse) and generate JSON.


## Use case

- transmit data across a network

## Getting data from an API

1. Use XHR
2. Store data URL in a variable
3. Create a new request object instance from the XMLHttpRequest constructor, using the new keyword.
  1. `var request = new XMLHttpRequest();``
4. Ppen a new request using the open() method.
  1. `request.open('GET', requestURL);`
5. Set the responseType to JSON, so that XHR knows that the server will be returning JSON, and that this should be converted behind the scenes into a JavaScript object.
  1. `request.responseType = 'json';`
6. Send the request via the send method:
  1. `request.send();`
7. Wait for the response to return from the server, then deal with it:
```
request.onload = function() {
  var superHeroes = request.response;
  populateHeader(superHeroes);
  showHeroes(superHeroes);
}
```
Here we are storing the response to our request (available in the response property) in a variable called superHeroes; this variable will now contain the JavaScript object based on the JSON! We also fill <header> and <section> with data




## Links

- [Validate JSON format](https://jsonlint.com/)
