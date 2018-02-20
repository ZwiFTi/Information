## Use case

- Working with information from ajax requests
- Posting messages back and forth between the main thread and a web worker
- Create a promise to run on interactive state is really useful if you want to run some code as all of the initial dom elements have been loaded.

## Syntax

```
new Promise(function(resolve) {
  console.log('first');
  resolve();
  console.log('second');
}).then(function() {
  console.log('third');
});
```

1. Pass a function to the promise with two arguments:
  1. Resolve
  2. Reject

[SYNTAX](https://www.youtube.com/watch?v=ikoar93RWe4)
