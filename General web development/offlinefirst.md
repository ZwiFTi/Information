# Description

If there is some kind of network failure, you do not want to leave the user with nothing. Get as many things on the screen as possible, using stuff already on the users device in caches and such.

# How?

1. Deliver content from a cache first, then
2. attempt to fetch updated content from the network
3. Use serviceworker!

# Serviceworker

- Serviceworker will only control pages within its scope

1. Pass in url of the script
```
if (!navigator.serviceWorker) return;
navigator.serviceWorker.register('/sw.js').then(function() {
  console.log('Registration worked!');
  }).catch(function() {
    console.log('Registration failed!');
    });

// if statement makes sure that it does not load if browser doesnt handle serviceWorker
```

2. add fetch to sw.js (catches all the requests made by user!)

```
self.addEventListener('fetch', function(event) {
  console.log(event.request);
  });
```

# Cache time

Cache time should be zero on all your service worker projects!

#
