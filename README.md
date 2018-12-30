# JavaScript Fundamentals

## Variables
 Variables are a container used to store data.

 The most used keywords for variables are __let__ and __const__. 

 __let__ variables allow you to change the assigned value, whereas __const__ variables cannot be changed later in code.

Example no. 1 using `let`: 

```javascript
let message = 'Hello!'; // define the variable and assign the value
``` 

Example no. 2 using `let`:

*We can also declare multiple variables*

```javascript
let user = 'John';
let age = 25;
let message = 'Ola';
``` 

## Variables naming

There are two limitations for a variable name in JavaScript:

1. The name must contain only letters, digits, symbols `$` and `_`.
2. The first character must not be a digit.

*When the name contains multiple words, [camelCase](https://en.wikipedia.org/wiki/Camel_case) is used. Meaning each word starts with a capital letter : `myNameIsRazvan`.


## Constants 

When declaring a value that will not be changed later on (constant), we use `const` keyword:

```javascript
const myBirthday = '18.04.1982';
``` 

## Upercase constants

Constants are usually used as aliases for difficult-to-remember values that are known prior to execution. 

Such constants are named using capital letters and uderscores, like this: 

```javascript
const COLOR_RED = "#F00";
const COLOR_GREEN = "#0F0";
const COLOR_BLUE = "#00F";
const COLOR_ORANGE = "#FF7F00";

// ...when we need to pick a color
let color = COLOR_ORANGE;
```
