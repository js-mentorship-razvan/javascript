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



## Operators

Most operators are similar to the ones we used in school, like : `+` to add, `*` to multiply, `-` to subtract, etc.


#### Terms: "unary", "binary", "operand"

Operators are applied to __operands__ Example: ` 9 * 7 `  -> we have left operator which is 9 and right operandor which is 7.
Operands are also sometimes called 'arguments'.

__unary__ means that an operator has a single operand. 

```javascript
let dry=5
dry = -5;
console.log(dry); // output will be -5 and the operator is unary 
```

__binary__ means that an operator has 2 operands.

```javascript
let a = 5, b = 8;
console.log(a-b); // output will be -3 and the operator is binary
```


#### Strings concatenation, binary + 

If `+` is applied to strings, it concatenates (merges) them. Example:

```javascript
let razvan = 'my' + ' name';
console.log(razvan); // my name
```

Note: If either operand is a string, then the output will be a string too and the operations run from left to right. Example:

```javascript
alert(4+2+'6'); // '66' and not '426' 
``` 

#### Numeric conversion, unary +

Unary + or `+` operator when applied to an operand that is not a number, it converts it into one. Example:

```javascript
let great = 2;
alert(+great); // 2 . Nothing happens because the operand is a number

let amazing = true;
alert(+amazing); // 1 . It has changed it into a number
```

It acts the same as `Number(..)`, but its shorter. Example:

```javascript
let beers = 6;
let wine = 2;
alert(+beers + +wine); // 8
alert(Number(beers) + Number(wine)); // 8 - same output, longer variant.
```

#### Operators precedence

Just like in school where multiplication is calculated first in this example `2 + 5 * 9`, the __higher precedence__ acts the same in JavaScript. 

Parantheses override any precedence and we can learn more about order [in here].(https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence) 

#### Assignment

An assignment `=` is also an operator. It is possible to do simple calculations and even chain assignments. Example:

```javascript
let i = 8 * 8 + 9;
alert(i); // 73  - simple calculation that returns a value stored in 'i' 
```

```javascript
let i,f,g;
i = f = g = 8 * 8;
alert(i); // 64
alert(g); // 64
```

#### Remainder %

The results of `b % c` is the _remainder_ of the integer division of `b` by `c`. Example: 

```javascript
alert (8 % 3); // 2 is the remainder of 8 divided by 3
```

#### Exponentiation **

The exponentiation operator `**` works for both integer and non-integer numbers. `b ** c` is `b` multiplied by itself `c` times. Example:

```javascript
alert ( 5 ** 5 ); // 3125
alert ( 2 ** 3 );  // 8
alert ( 9 ** (1/2) ); // 3 (power of 1/2 is the same as a square root from maths)
```

#### Increment/decrement

`++` increment increases a variable by 1:

```javascript
let measure = 5;
measure ++; 
alert(measure); // 6 
```

`--` decrement decreases a variable by 1:

```javascript
let measure = 5;
measure --;
alert(measure); // 4 
```

__Increment and decrement can only be applied to a variable!__

These `++` and `--` operators can be placed both after and before the variable. When used before the variable its called "prefix form" and if used after the variable its called "postfix form". 

- If the result of increment/decrement is not used, then both forms gives the same results;
- If the result of increment/decrement is used now, we need the prefix form;
- If we need to use the old result, then we need the postfix form. 

