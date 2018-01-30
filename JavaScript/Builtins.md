# Built ins in JavaScript
# TODO: Course 898 on promises

## Table of Contents

1. [Description](#description)

2. [Sets](#construction)
  1. [Construction](#construction)
  2. [Use case](#construction)
  3. [Add - Delete - Modify - Loop](#construction)
  4. [Properties and Methods](#construction)

3. [WeakSet](#construction)
  1. [Construction](#construction)
  2. [Use case](#construction)
  3. [Add - Delete - Modify - Loop](#construction)
  4. [Properties and Methods](#construction)

4. [Maps](#construction)
  1. [Construction](#construction)
  2. [Use case](#construction)
  3. [Add - Delete - Modify - Loop](#construction)
  4. [Properties and Methods](#construction)

5. [WeakMap](#construction)
  1. [Construction](#construction)
  2. [Use case](#construction)
  3. [Add - Delete - Modify - Loop](#construction)
  4. [Properties and Methods](#construction)

5. [Promises](#construction)
  1. [Construction](#construction)
  2. [Use case](#construction)
  3. [Add - Delete - Modify - Loop](#construction)
  4. [Properties and Methods](#construction)

5. [Proxies](#construction)
  1. [Construction](#construction)
  2. [Use case](#construction)
  3. [Add - Delete - Modify - Loop](#construction)
  4. [Properties and Methods](#construction)

5. [Generators](#construction)
  1. [Construction](#construction)
  2. [Use case](#construction)
  3. [Add - Delete - Modify - Loop](#construction)
  4. [Properties and Methods](#construction)

## 1.0 Description



## 2.0 Sets

- Array-like
- not index based
- items in a set cant be accessed individually
- Automatically Removes duplicate entries

### Construction

Option 1:
```
const games = new Set();
console.log(games);

// Set {}

```

Option 2: List of values (array)
```
const games = new Set(['Super Mario Bros', 'Banjo-Kazooie', 'Mario Kart']);
console.log(games);

// Set {'Super Mario Bros', 'Banjo-Kazooie', 'Mario Kart'}


```

### Use case






### Add, delete, modify, loop

.add() and .delete() // add delete individual items
.clear() // delete all items

loop:
1. Sets default iterator
  const iterator = months.values();
  iterator.next(); //use this until true
2. for...of loop (easiest)
  for (const color of colors) {
    console.log(color);
  } // use this where colors is the Sets name

### Properties and methods

Properties
.size //return the number of items in a Set


Methods
.has() // check if item exists in a Set
.values() // return the values in a Set





## 3.0 WeakSet

- Just like Set with few differences:
- Can only contain objects
- Not iterable (can't be looped over)
- does not have .clear() method

### Construction

```
const student1 = { name: 'James'};
const student2 = { name: 'Julia'};
const student3 = { name: 'Richard'};

const roster = new WeakSet([student1, student2, student3]);
console.log(roster);

// WeakSet {Object {name: 'Julia'}, Object {name: 'James'}, Object {name: 'Richard'}}

```

### Use case

Use on objects instead of Sets because of garbadge collection! Its good for memory. set an object to null to delete it. student3 = null;

When an object is deleted, the object will also be deleted from the WeakSet when garbage collection runs. Its a efficient lightweight solution for creating groups of objects.


### Add, delete, modify, loop



### Properties and methods

Properties


Methods


## 3.0 Maps

A map is an object that lets you store key-value pairs where both the keys and the values can be objects,

### Construction

Empty map with no key-value pairs
```
const employees = new Map();
console.log(employees);

// Map {}
```


### Use case



### Add, delete, modify, loop

To add, create key-values by using .set() method

```
employees.set('james.parkes@udacity.com', {
  firstName: 'James',
  lastName: 'Parkes',
  role: 'Content Developer'
  })
```

To delete an individual, use the .delete() method
employees.delete('james.parkes@udacity.com');


To delete all: .clear()

Loops:

1. Maps default iterator
  ```
  let iteratorObjForKeys = members.keys();
  iteratorObjForKeys.next();
  ```
2. for...of loop
  ```
  for (const member of members) {
    console.log(member);
  }
  ```
3. .forEach() method
  `members.forEach((key,value) => console.log(key, value));`


### Properties and methods

Properties


Methods
.has() // Check if a key-value pair exists in your Map by passing it a key


## 5.0 Promises

A promise will let you start some work that will be done asynchronously and let you get back to your regular work.

A Promise constructor takes a function that will run and then, after some amount of time, will either complete successfully (using the resolve method) or unsuccessfully (using the reject method). When the outcome has been finalized (the request has either completed successfully or unsuccessfully), the promise is now fulfilled and will notify us so we can decide what to do with the response.

1. A Promise will immediately return an object.

### Construction


```
new Promise(function () {
  window.setTimeout(function createSundae(flavor = 'chocolate') {
    const sundae = {};
      // request ice cream
      // get cone
      // warm up ice cream scoop
      // scoop generous portion into cone!
    }, Math.random() * 2000);
  });
```

resolve: The resolve method is used to indicate that the request is complete and that it completed successfully.

reject: is used when the request could not be completed.

### Use case


### Add, delete, modify, loop


### Properties and methods

Properties


Methods

## 6.0 Proxies

A proxy object sits between a real object and the calling code. The calling code interacts with the proxy instead of the real object.

### Construction
The proxy constructor takes two items,
1. the object that it will be the proxy for
2. an object containing the list of methods it will handle for the proxied object

```
var richard = {status: 'looking for gf'};
var agent = new Proxy(richard, {});

agent.status; //returns looking for work'
```

Tp create a proxy:
1. Use the new Proxy() constructor
2. Pass the object being proxied as the first item
3. The second object is a handler object
4. The handler object is made up of 1 of 13 different traps
5. A trap is a function that will intercept calls to properties let you run code
6. If a trap is not defined, the default behavior is sent to the target object.

### Use case

The key to making Proxies useful is the handler object that's passed as the second object to the Proxy constructor. The handler object is made up of a methods that will be used for property access. (as with get).

Its a powerful way to create and manage interactions between objects!

get: Take over whenever any property on the proxy is accessed
set: Used for intercepting code that will change a property

### Traps

Get trap:
```
const richard = {status: 'looking for work'};
const handler = {
    get(target, propName) {
        console.log(target);
        console.log(propName);
        return target[propName];
    }
};
const agent = new Proxy(richard, handler);
agent.status; // (1)logs the richard object, (2)logs the property being accessed, (3)returns the text in richard.status
```

Set trap:
```
const richard = {status: 'looking for work'};
const handler = {
    set(target, propName, value) {
        if (propName === 'payRate') { // if the pay is being set, take 15% as commission
            value = value * 0.85;
        }
        target[propName] = value;
    }
};
const agent = new Proxy(richard, handler);
agent.payRate = 1000; // set the actor's pay to $1,000
agent.payRate; // $850 the actor's actual pay
```
Other traps:

- the get trap - lets the proxy handle calls to property access
- the set trap - lets the proxy handle setting the property to a new value
- the apply trap - lets the proxy handle being invoked (the object being proxied is a function)
- the has trap - lets the proxy handle the using in operator
- the deleteProperty trap - lets the proxy handle if a property is deleted
- the ownKeys trap - lets the proxy handle when all keys are requested
- the construct trap - lets the proxy handle when the proxy is used with the new keyword as a constructor
- the defineProperty trap - lets the proxy handle when defineProperty is used to create a new property on the object
- the getOwnPropertyDescriptor trap - lets the proxy handle getting the property's descriptors
- the preventExtenions trap - lets the proxy handle calls to Object.preventExtensions() on the proxy object
- the isExtensible trap - lets the proxy handle calls to Object.isExtensible on the proxy object
- the getPrototypeOf trap - lets the proxy handle calls to Object.getPrototypeOf on the proxy object
- the setPrototypeOf trap - lets the proxy handle calls to Object.setPrototypeOf on the proxy object


### Properties and methods

Properties


Methods




## 6.0 Generator functions

function* indicates that the function is a generator function.

### Construction

How to write it:
```
function* getEmployee() {
    console.log('the function has started');

    const names = ['Amanda', 'Diego', 'Farrin', 'James', 'Kagure', 'Kavita', 'Orit', 'Richard'];

    for (const name of names) {
        console.log( name );
    }

    console.log('the function has ended');
}
```


How to run it:
```
const generatorIterator = getEmployee();
generatorIterator.next();
```


How to pause it:
Place `yield;` inside the for loop in the function*

How to get data out:
Place `yield data-we-want-returned;`. This could be `yield name;` in the generator function above.

How to get data into the function:
```
function* displayResponse() {
    const response = yield;
    console.log(Your response is "${response}"!);
}

const iterator = displayResponse();

iterator.next(); // starts running the generator function
iterator.next('Hello Udacity Student'); // send data into the generator
// the line above logs to the console: Your response is "Hello Udacity Student"!
```

### Use case

If we want to pause a function mid-execution, we need generator functions. Great for:

1. Iterating over a list of items one at a time so you can handle each item on its own before moving on to the next one
2. To handle nested callbacks

### Properties and methods

Properties


Methods
