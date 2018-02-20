
## Links
[MDN's docs](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest/open)
[WHATWG Spec](https://xhr.spec.whatwg.org/)
[W3C Spec](https://www.w3.org/TR/XMLHttpRequest/)


## SYNTAX

```
function handleSuccess () {
  console.log( this.responseText );
// the HTML of https://unsplash.com/}
function handleError () {
  console.log( 'An error occurred \uD83D\uDE1E' );
}
const asyncRequestObject = new XMLHttpRequest();
asyncRequestObject.open('GET', 'https://unsplash.com');
asyncRequestObject.onload = handleSuccess;
asyncRequestObject.onerror = handleError;
asyncRequestObject.send();
```


## Convert JSON response to JavaScript object

```
function handleSuccess () {
const data = JSON.parse( this.responseText ); // convert data from JSON to a JavaScript object
console.log( data );
}

asyncRequestObject.onload = handleSuccess;
```


## To Send An Async Request

* create an XHR object with the XMLHttpRequest constructor function
* use the .open() method - set the HTTP method and the URL of the resource to be fetched
* set the .onload property - set this to a function that will run upon a successful fetch
* set the .onerror property - set this to a function that will run when an error occurs
* use the .send() method - send the request

## To Use The Response

* use the `.responseText` property - holds the text of the async request's response
