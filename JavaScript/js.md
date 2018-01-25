TODO: https://www.udacity.com/course/es6-javascript-improved--ud356

# Syntax

### Loops
`for (var i = 0; i < 10; i++) {
  console.log(i);
}`

### Print to Console
`console.log("foo");`

### comments
` /* ... */` or `// this is a single line comment`

### Variable assignment
`var variableName = value;``

### Get element and do something with it
`document.getElementsByTagName("h1")[0].style.color = "#ff0000";`

### Escaping characters

use: `\` backslash

### if-else statement

`if (/* this expression is true */) {
  // run this code
} else {
  // run this code
}`

By adding the extra `else if` statement, you're adding an extra conditional statement.

ternary operator:
`conditional ? (if condition is true) : (if condition is false)`, example:

`isGoing ? "green" : "red";`

switch statement:
`switch (option) {
  case 1:
    console.log("You selected option 1.");
  case 2:
    console.log("You selected option 2.");
  case 3:
    console.log("You selected option 3.");
  case 4:
    console.log("You selected option 4.");
  case 5:
    console.log("You selected option 5.");
  case 6:
    console.log("You selected option 6.");
}` (can also add break and default to switch statements)

### Logical operators

* `&&`: AND
* `||`: OR
* `!` : NOT

### the ONLY 6 falsy values in JS

1. the Boolean value false
2. the null type
3. the undefined type
4. the number 0
5. the empty string ""
6. the odd value NaN (stands for "not a number", check out the NaN MDN article)

# Datatypes

1. Number (1, 2, etc)
2. Booleans (true or false)
3. Strings (text)
4. null (value of nothing, totally empty)
5. undefined (absence of value, does not have a value)



### Checklist

1. All strings have singlequotes
2. Variable names are camelCase
3. Minimize the amount of global variables
4. Declare functions and variables at the top of your scripts, so the syntax and behavior are consistent with each other.


# Reference list

Special characters: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Using_special_characters_in_strings
