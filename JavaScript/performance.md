These are the steps to use performance.now() to measure the speed of your code:

use performance.now() to get the an initial start time for the code
run the code you want to test
execute performance.now() to get another time measurement
subtract the initial time from the final time


# Time your code

<!-- Before code -->
const startingTime = performance.now();

<!-- Code to test -->

<!-- After code -->

const endingTime = performance.now();
console.log('This code took ' + (endingTime - startingTime) + ' milliseconds.');

# Stop DOM from repainting on every element

const fragment = document.createDocumentFragment();  // ← uses a DocumentFragment instead of a <div>

for (let i = 0; i < 200; i++) {
    const newElement = document.createElement('p');
    newElement.innerText = 'This is paragraph number ' + i;

    fragment.appendChild(newElement);
}

document.body.appendChild(fragment); // reflow and repaint here -- once!


# Running code later

.addEventListener()
setTimeout()

The `setTimeout()` function takes:

- a function to run at some later time
- the number of milliseconds the code should wait before running the function

setTimeout(function sayHi() {
    console.log('Howdy');
}, 1000);

You use setTimeout() so that user can interact with your page without beeing frozen up. You have to read more on this

# Best way to make group of changes

In general, if you have to make a group of changes, hide/change all/show is a great pattern to use if the changes are relatively contained.

# EVENT LOOP

https://youtu.be/uBdemYBG-ek

IMPORTANT: The key things to remember here are 1) current synchronous code runs to completion, and 2) events are processed when the browser isn't busy. Asynchronous code (such as loading an image) runs outside of this loop and sends an event when it is done.

https://www.youtube.com/watch?v=8aGhZQkoFbQ



# references

- https://www.udacity.com/course/website-performance-optimization--ud884

- https://www.udacity.com/course/browser-rendering-optimization--ud860

- https://developers.google.com/speed/docs/insights/browser-reflow

- https://developers.google.com/web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing

- https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/reference#rendering

- http://www.stubbornella.org/content/2009/03/27/reflows-repaints-css-performance-making-your-javascript-slow/
