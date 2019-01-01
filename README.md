# JavaScript Fundamentals


## Variables
 Variables are a container used to store data.

 The most used keywords for variables are __let__ and __const__. 

 __let__ variables allow you to change the assigned value, whereas __const__ variables cannot be changed later in code.

Example no. 1: 

```javascript
let message = 'Hello!'; // define the variable and assign the value
``` 

Example no. 2:

*We can also declare multiple variables*

```javascript
let user = 'John';
let age = 25;
let message = 'Ola';
``` 

### Variables naming

There are two limitations for a variable name in JavaScript:

1. The name must contain only letters, digits, symbols `$` and `_`.
2. The first character must not be a digit.

*When the name contains multiple words, [camelCase](https://en.wikipedia.org/wiki/Camel_case) is used. Meaning each word starts with a capital letter : `myNameIsRazvan`.*


### Constants 

When declaring a value that will not be changed later on (constant), we use `const` keyword:

```javascript
const myBirthday = '18.04.1982';
``` 

### Upercase constants

Constants are usually used as aliases for difficult-to-remember values that are known prior to execution. 

Such constants are named using capital letters and uderscores, like this: 

```javascript
const COLOR_ORANGE = "#FF7F00";
// ...when we need to pick a color
let color = COLOR_ORANGE;
```



## Data types

There are 7 basic data types:

1. __number__ 

*for any kind of numbers*

Example: 

```javascript
let n = 94;
n = 19.94;
```

2. __string__ 

*we will find it in between quotes (single quotes `''`, double quotes `""` ) or backticks ` `` `.*

Example:

```javascript
let name = 'Razvan';
let dog = "Husky";
let longPhrase = `My dog's owner is ${name}`;
```

3. __boolean__ 

*can only express `true` and `false`.*

Example:

```javascript
let myIphoneIsXs = true;  // yes, I have an Iphone Xs
let myOldIPhone = false; // no, I didn't have any other Iphone
```

4. __null__ 

*it has a special value of nothing / empty / unknown value.*

Example:

```javascript
let dog = null; // dog is unknown or empty
``` 

5. __undefined__ 

*the value of `undefined` is 'value not assigned'*

Example:

```javascript
let age;
console.log(age); // output will be *undefined*
```

6. __objects__ 

*`object` is a special data type used to store collections of data.*

7. __symbol__

*`symbol`is used to create unique identifiers for objects*


### typeof operator

 `typeof` returns the type of the argument. It can be used with or without parantheses and the result will be the same.

 Example:

 ```javascript
 typeof 'animal' // output will be "string"
 typeof '241.94' // output will be "string"
 typeof 95 // output will be "number"
 ```



## Type Conversions 

### ToString

*is used to convert a value to a string form* 

Example: 

```javascript
let name = true;
alert(typeof name); // output will be 'boolean'

name = String(name); // output will be a string 'true'
alert(typeof name); // output will be 'string'
```

### ToNumber

*In mathematical functions and expressions, numeric conversion happens automatically*

*`Number(value)` function is used to convert a value. For example:*

```javascript
let word = '88';
alert(word); // output will be a string

let wordToNumber = Number(word); 
console.log(wordToNumber); // output will be a number : 88 
```

#### Numeric Conversion

```javascript
alert( Number(   " 999 "   )); // output will be a number : 999
alert( Number("765z"));        // output will be : NaN(not a number) because of 'z' letter at the end
alert( Number(true));          // output will be a number : 1 
alert( Number(false));         // output will be a number : 0
```

All mathematical operations convert values to numbers, except `+`. If one of the value has a string form, the other values are also converted to string when using `+` operator. Example: 

```javascript
alert ('54' + 26); // output will be a string : '5426'
```

### ToBoolean

*Any value that's 'empty' fe: 0, an empty string, null, undefined, NaN become `false`. All other values convert to `true`.* Example:

```javascript
alert( Boolean(41)); // output will be true
alert( Boolean("")); // output will be false
```
