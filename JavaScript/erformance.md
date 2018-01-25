These are the steps to use performance.now() to measure the speed of your code:

use performance.now() to get the an initial start time for the code
run the code you want to test
execute performance.now() to get another time measurement
'subtract the initial time from the final time
'

# How to

<!-- Before code -->
const startingTime = performance.now();

<!-- Code to test -->

<!-- After code -->

const endingTime = performance.now();
console.log('This code took ' + (endingTime - startingTime) + ' milliseconds.');
