## Description

You make request for some data, and then without pausing for everything to wait for the request to return, you just move on and do something else. When the request does get returned, you deal with it.

## Use case

- Ajax requests allow for content retrieval and display without reloading the web page.

## Handle asynchronous requests with jQuery

1. Use the `.ajax()` method
2.

```
function handleResponse(data) {
    console.log('the ajax request has finished!');
    console.log(data);
}

$.ajax({
    url: 'http://swapi.co/api/people/1/'
}).done(handleResponse);
```

### Syntax

```
$.ajax(<url-to-fetch>, <a-configuration-object>);

// or

$.ajax(<just a configuration object>);
```

## Handle requests with fetch

```
fetch(`https://api.unsplash.com/search/photos?page=1&query=${searchedForText}`, {
    headers: {
        Authorization: 'Client-ID abc123'
    }
}).then(function(response) {
    debugger; // work with the returned response
});
```

### Use arrow functions!!

```
// without the arrow function
}).then(function(response) {
    return response.json();
})

// using the arrow function
}).then(response => response.json())
```

### FULL EXAMPLE
```
fetch(`https://api.unsplash.com/search/photos?page=1&query=${searchedForText}`, {
    headers: {
        Authorization: 'Client-ID abc123'
    }
}).then(response => response.json())
.then(addImage)
.catch(e => requestError(e, 'image'));

function addImage(data) {
    debugger;
}

function requestError(e, part) {
    console.log(e);
    responseContainer.insertAdjacentHTML('beforeend', `<p class="network-warning">Oh no! There was an error making a request for the ${part}.</p>`);
}
```


### Changing methods

```
fetch(`https://api.unsplash.com/search/photos?page=1&query=${searchedForText}`, {
    method: 'POST'
});
```

### Links
https://developer.mozilla.org/en-US/docs/Web/API/GlobalFetch/fetch
https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch
https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API
https://fetch.spec.whatwg.org/#methods
https://fetch.spec.whatwg.org/#requests
https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch#Making_fetch_requests
https://davidwalsh.name/fetch
