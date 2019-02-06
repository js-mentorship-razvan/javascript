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

Parantheses override any precedence and we can learn more about order [in here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence) 

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
measure++; 
alert(measure); // 6 
```

`--` decrement decreases a variable by 1:

```javascript
let measure = 5;
measure--;
alert(measure); // 4 
```

__Increment and decrement can only be applied to a variable!__

These `++` and `--` operators can be placed both after and before the variable. When used before the variable its called "prefix form" and if used after the variable its called "postfix form". 

- If the result of increment/decrement is not used, then both forms gives the same results;
- If the result of increment/decrement is used now, we need the prefix form;
- If we need to use the old result, then we need the postfix form. 

Examples: 

```javascript
let distance = 6;
let newDistance = ++distance;
alert(newDistance); // 7 - it returns the new value
```

```javascript
let distance = 6
let newDistance = distance++;
alert(newDistance); // 6 - it returns the old value
```

#### Modify-in-place

It is used to store the new result of an operator applied to a variable. Example:

```javascript
let f = 5;
f = f + 6; // result is 11 ( 5 + 6)
f = f * 2; // result is 22 ( 11 * 2)
``` 
We can write the same lines of code using `+=` and `*=` operators: 

```javascript 
let f = 5;
f += 6; // 11 ( same as above where f = f + 6 )
f *= 2; // 22 ( same as above where f = f * 2 )
```

## Comparisons

Some comparisons signs are similar to those we have in maths, like:

* Greater/ less than : ```a > b``` and ```a < b```;
* Greater/ less than or equals : ``` a >= b ``` and ``` a <= b ```;
* Equals : ```a == b``` //  notice the difference between = and double == ; 
* Not equals : ```a != b``` 
* Greater/ less than : ``` a > b ``` and ``` a < b ```;
* Greater/ less than or equals : ``` a >= b ``` and ``` a <= b ```;
* Equals : ``` a == b ``` //  notice the difference between = and double == ; 
* Not equals : ``` a != b ``` 

#### Boolean comparison

A comparison returns a value, in this case the returned value is a boolean. Example:

```alert ( 2 > 1 ); // true```
```alert ( 2 > 1 ); // true ```

```let dog = 5 != 4; 
alert(dog); // true because 5 is does not equal 4
```

#### String comparison

Strings are compared letter by letter in JavaScript according to [Unicode order](https://www.w3.org/TR/xml-entity-names/bycodes.html). Example:

```alert ( 'Razvan' > 'Andrei' ); // true because R > A```

#### Different types comparison

Values are converted to numbers when different types are compared. For boolean ```true``` becomes ```1``` and ```false``` becomes ```0```. Example:

```alert ( true == 1 ); // true because 1 = 1 ```  <- boolean compared with number;

```alert ( 5 == '5' ); // true because string is converted to number``` <- string compared with number;

#### Strict equality

A strict equality check ```===``` compares values without any type conversion. It is used because equality check ```==``` cannot differentiate ```0``` from ```false``` or an empty string ```''``` from ```false```

#### Comparison with null and undefined 

__If we use ```==``` for ```null``` and ```undefined```, the result will be ```true``` and they don't equal anything else when checked for equality!__

```alert(null==undefined)``` 

*This is only true when we check for equality.*

When checked for other comparisons, ```null``` becomes ```0``` and ```undefined``` becomes ```NaN```



## Interaction: alert, prompt, confirm 

#### alert 

When `alert` is called, a mini-window appears on the screen, which is called *modal window*. This will block the user to interact with the rest of the page until this window is dealt with.

```javascript
alert('My name is Razvan');
```

#### prompt 

`prompt` accepts two arguments and it gives the user the possibility to input something. In this case, the modal window will have a *text* message that is seen by the user and a *default* parameter which is the initial value for the imput field and is optional. Example: 

```javascript
let dog = prompt('How many dogs do you have?', 1);  // string being the displayed text and 1 the initial value
alert(`You have ${dog} dog/s`);
```

#### confirm

`confirm` displays a modal window with a question and two buttons : OK and Cancel. It returns `true` if OK is pressed and `false` otherwise. Example:

```javascript
let question = confirm('Is the computer you are typing from yours?');
alert(question); // true if OK is pressed, false otherwise.
```

## Conditional operators: if, "?" 

We use `if` and `?` when we need to execute some actions based on some conditions. 

When condition is `true` inside an `if` statement, the engine will execute the block of code inside the `{}`. For example: 

```javascript
let myName = 'Razvan';
if (myName !== 'Razvan') {
    return 'Nah, try again, please.';
}
```

The `if` statement evaluates the expression in ith parentheses and converts the result to a boolean. 

#### The "else" clause 

`else` block is an optional keyword for `if` statements. It is only executed when the condition is `false`. For example: 

```javascript
let iphone = prompt('What is the name of the company that produces iphone smartphones?');
if (iphone == 'Apple') {
    return 'Well done!';
} else {
    return 'That is not quite right.'
}
}
```

#### Several conditions: "else if"

In case we want to test more than one condition, `else if` is used and it allows us to do just that. 

#### Ternary operator "?"

Ternary operator `?` lets us assign a variable depending on a condition. It is also the only operator in JavaScript that has three operands.
Example:

```javascript
let question = condition ? value1 : value; // this is how the syntax looks
```

```javascript
let accessAllowed;
let location = prompt('Are you from Europe?', '');

if (location == 'yes') {
  accessAllowed = true;
} else {
  accessAllowed = false;
}

alert(accessAllowed);
```

#### Multiple "?"

A sequence of question mark operators `?` can return a value that depends on more than one condition. Example: 

```javascript
let location = prompt('Where are you from?', 'Europe') 

let message = (location == 'Europe') ? 'Welcome' :
  (location == 'US') ? 'Wazzap, Mr. Trump?' : 
  (location == 'Asia') ? 'I hope I can learn chineese some day' :
  'Never been there before.';

  alert(message);
  ```


  ## Logical operators

  In JavaScript, there are three logical operators `||` (OR), `&&` (AND), `!` (NOT). They can be applied to values of any type!

  #### || (OR)

   The 'OR' operator is represented by two vertical line symbols `||`. It's job is to look for any `true` value and it will return `true` when it finds it, otherwise will return `false`. 

```javascript
let a = 1;
let b = 0; 
alert (a || b); // will return 1 becasue is true and 0 is false;
```

The OR operator is converting everything to boolean, then is looking for the first `true` value and returns it. If no such value is found, it returns the last value. Example: 

```javascript
let name = undefined;
let nob = null; 
let age = 0; 

alert (undefined || null || 0); // will return 0 because none of these values are true when converted to boolean.
```

#### && (AND)

The AND operator is represented by two ampersands `&&`. This operator will return `true` if all operands are truthy and `false` otherwise. When a falsy value is found, it will return the first value, no matter how many falsy values we have. 

The AND operator evaluates operands from left to right ( like OR), then converts all values to boolean and compare them (like OR) and returns the original value of the first falsy value when found. If all values are truthy, it returns the original value of the last operand. Examples:

```javascript
let hour = 15;
let minute = 35;

if (hour == 15 && minute == 35) {
  alert( 'The time is 15:35' ); // - Will return this string because both values are truthy
}
```

```javascript
alert (1 && 0 && null && undefined); // will return 0 because that is the first falsy value.
```

## Precedence of AND `&&` is HIGHER than OR `||`

#### ! (NOT)

The NOT operator is represented by exclamation sign `!`. It accepts a single argument and converts the operand to boolean and returns the inversed value. Example: 

```javascript
alert ( !1 ); // will return false because 1 is true, and the inversed value of true is false
``` 

## Loops: while and for

Loops are a way to repeat the same code multiple times.

#### "while" loop 

While the condition (what is inside the parantheses) is `true`, the code that is inside the body loop is executed. Example : 

```javascript
let i = 5; 
while (i);
alert (i); // code will show 4,3,2,1 then it stops because 0 is falsy and so the condition is not met anymore;
i--;
```

The above code can be written like this too: 

```javascript
let i = 5;
while (i < 5) {
    alert (i);
    i--;
}
```

`i++` or `i--` is used so that the loop will know when to stop, otherwise we will have an infinite loop and our code won't work properly. 

#### "do...while" loop 

When using this loop, the code will execute first time without checking any conditions, only after running once will check the condition and if `true` will run again, else will stop. Example : 

```javascript
let i = 5; 
do {
    alert(i);
    i--;
} while (i > 2); // code will show 5,4 and 3 because 2 = 2 and condition becomes falsy.
```

This condition is used when we want to execute the code once regardless of the condition. But, the preferred loop is `while(...) {...}`.

#### "for" loop

This is the most used loop. This loop contains `(begin; condition; step)` and then it has the code inside the body. 

This is how it works: 
1. Run begin;
2. if condition is true -> run body and run step;
3. if condition is true -> run body and run step;
4. and so on until condition becomes falsy.

Any part of the `for` loop can be skipped. If we delete all parts, then we will have an infinite loop : 
```javascript
for (;;){
    // repeats without limits
}
```
Example of for loop: 

```javascript
for (let i = 0; i < 5; i++) {
    alert(i); // code will show 0,1,2,3,4 and stops when it gets to 5 because condition becomes falsy
}
```

The condition becoming falsy is NOT the only way to stop a loop. Using the special `break` directive will achieve the same result. Example: 

```javascript
for (let i = 0; i < 5; i++) {
    if ( i == 3) break;
    alert(i);
}
alert(" This string will show when break is activated. ");
```

When `break` is activated, the engine will execute the next line of code after the loop. See above.

Another special directive is `continue` which is a ligher version of `break`. When `continue` is activated, the loop won't be stoped all together, but instead, it just stops the current iteration and forces the loop to start a new one if condition is truthy. Example: 

```javascript
for (let i = 0; i < 14; i++) {
    if (i % 2 !== 0) continue;
    alert(i); // will show 0,2,4,6,8,10,12
}
```


## The "switch" statement

A `switch` statement can be a replacement for multiple "if" checks. It contains one or more `case` blocks and an optional `default`.

Example:

```javascript
let a = 2 + 8;

switch (a)  {
    case 1:
    alert ('Way to small');
    break;
    case 5:
    alert ('You are getting closer but still small');
    break;
    case 9:
    alert ('Really hot!');
    break;
    case 10:
    alert ('You got it!');
    break;

    default:
    alert ('What value is that?!');
}
```
Let's examine how the `switch` statement works: 
1. a = 10 as described in our global variable above.
2. Now , the switch starts to replace `a` value in every case and it compares the values.
3. It runs every case until a match is found.
4. When the match is found, it executes the line of code for that case.
5. If there is a `break;` statement, then it stops. 
6. If there is no `break;` statement after the match, it keeps executing the next cases without stopping.
7. In case of *no match*, then the `default` code is executed.

Very important :
1. **Any expression can be a `switch/ case` argument!!!**
2. **The equality check is always strict! Values must be the same type to match.**



## Functions

Functions allow users to write code that can be used in many places of the script. They allow the code to be called many times without repetition. Some built-in functions include `alert(message)`, `prompt(message, default)` and `confirm(question)`. Let's see how we can create functions of our own.

Example of a simple function : 

```javascript
function hiThere() {
    alert('Hello and welcome! I hope you will enjoy your time with us!');
}
hithere();
hithere(); 
hithere();
```  

Now let's explain the function above and how it works :
1. A function starts with the `function` keyword followed by the name, in this case we named our function `hiThere`.
2. After it's name, in parentheses we can include parameters. Parameters are usually generic, so that we can use the function with multiple values without writing it again, this is the whole purpose of a function in the first place.
3. Then, in between the curly brakes `{}` we write the "function body" which is nothing else than the code that the function will execute.
4. To call a function, we write it's name and the given parameters outsite it's body. Just like above. 

*Functions can use global variables or have they own local variables. The difference between them is that local variables can only be used inside the function whereas the global ones can be used anywhere in our code.*

Example of function with parameters(also called arguments): 

```javascript
function sum(a, b) {
    alert (a + b);
}
sum(8, 2); // output will be 10 
sum(21, 4); // output will be 25
```

As we  can see in the example above, the arguments `a` and `b` are given some values and the function executes the code `alert (a + b)`.

### Returning a value

A function accepts `return` directives in any place, multiple times if needed. For example :

```javascript
function checkAge(age) {
  if (age > 18) {
    return true;
  } else {
    return confirm('Do you have permission from your parents?');
  }
}

let age = prompt('How old are you?', 18);

if ( checkAge(age) ) {
  alert( 'Access granted' );
} else {
  alert( 'Sorry, try again when you are 18+' );
}
```

*Some important information about functions:*

* When naming a function, you should use a verb, because functions usually represents actions.
* A function name should be very brief and intuitive, such as `get`, `calc`, `show`, `create` etc.
* Never add a newline between `return` statement and the value. This is because in JS, it assumes a semicolon after `return` and the code will stop there. 
* A function with an empty `return` or without it, returns `undefined`  
 Example: 
 ```javascript
 function doNothing() {
    // empty in here
 } 
alert (doNothing() === undefined ); // will return true!
``` 
```javascript
function doNothing() {
    return;
}
alert (doNothing() === undefined ); // will return true as well
```
* A function should do exactly what is suggested by its name and no more. One function = One action



## Function expressions and arrows

Functions have 3 types of syntax in JavaScript. We have just seen _function declaration_ above, now we will dive intro _function expression_ and _arrow functions_. 

This is how the syntax for *Function Declaration* looks like: 

```javascript
function sayHi() {
    alert ('Salut');
} 
```
Now let's see the syntax for *Function Expression*: 

```javascript
let sayHi = function() {
    alert ('Salut');
};
``` 

And finally, the syntax for *Arrow Function*:

```javascript
let func = (arg1, arg2, ...argN) => expression
```

Which is equivalent to this, but is much more concise: 

```javascript
let func = function(arg1, arg2, ...argN) {
    return expression;
}
``` 

### *Now let's see when to use what kind of function and why*

1. As a rule of thumb, *Function Declaration* is the preferred syntax used in JavaScript. This is because it looks clean and it's easy to look up to and also we can call such functions before they are declared!
2. If a *Function Declaration* doesn't suit us for some reason, then we can use *Function Expressions* instead.
3. Arrow functions are handy for mostly one-line actions and callbacks. 

### Function Expressions

Function Expressions are created when the execution reaches them. 

**When a Function Declaration is made within a code block, it is visible everywhere inside that block, but NOT outside of it.**

Let's see an example with Function Expression: 

```javascript
let age = prompt("What is your age?", 18);

let welcome;

if (age < 18) {
  welcome = function() {
    alert("Hello!");
  };

} else {
  welcome = function() {
    alert("Greetings!");
  };
}
welcome(); 
``` 

In the example above, the code runs as expected because Function Expressions is stored in a variable that is outside of `if` and has global visibility. 


### Arrow functions

This type of functions are handy for one-liners (actions and callbacks) and they come in two types: 
- Without curly braces `(...args) => expression` - the right side is an expression. The function evaluates it and returns the result.
- With curly braces: `(...args) => { body }` - brackets allow us to write multiple statements inside the function, but we need to have a `return` statement to return something.

Example of arrow function: 

```javascript
let sum = (a, b, c) => {
    let result = a + b + c;
    return result;
}
alert( sum(1, 5, 4) ); // 10
``` 

And now an example without curly braces:

```javascript
let sum = (a, b, c) => a + b + c;
alert( sum(1, 5, 4) ); // 10
```


## JavaScript specials - Recap

#### Code structure

Statements are delimited with a semicolon: 
```javascript
alert('Hi, I am Razvan'); alert('This is a new statement');
```

*Semicolons are not required after code blocks `{}` and syntax constructs with them like loops:*
```javascript
function doNothing() {

} // no semicolon needed

for (;;) {

} // no semicolon needed 
```

### Variables

They can be declared using three keywords and they can store any value:
1. `let` - you can change it's stored value later in the code; 
2. `const` - constant, cannot be changed;
3. `var` - old-style.

*There are 7 data types:*

1. `number` for both floating-point and integer numbers;
2. `string` for strings;
3. `boolean` for logical values `true/false`;
4. `null` a type with a single value `null`, meaning empty or does not exist;
5. `undefined` a type with a single value `undefined`, meaning not assigned;
6. `object` and `symbol` - for complex data structures and unique identifiers.
7. `type of` - returns the type for a value.

### Interaction

- `prompt(question[, default])` - it is used to ask a question and the user input or `null` if cancel is pressed;
- `confirm(question)` - it is used to ask a question and suggest to choose between OK and Cancel. Answer is returned as `true/false`;
- `alert(message)` - it is used to display a message.

### Operators

* *Arithmetical* : `+, -, *, /, % and **` . The binary `+` concatenates strings as well.
* *Assignments* : `a = b` or `a *= 2` which is equal to `a = a * 2`.
* *Ternary* has three parameters: `cond ? resultA : resultB` - If cond is truthy, resultA is displayed, otherwise resultB.
* *Logical operators* : OR `||`, AND `&&`, NOT `!`. 
* *Comparisons*: We have to types of equality checks for comparisons, `==` converts the values to numbers and compares them and `===` compares the type and also the value without conversion.

### Loops 

There are 3 type of loops studied so far: 
1. ```javascript
    while (condition) {
        ... body 
    }
    ``` 
2. ```javascript
    do {
        ... body
    } while (condition);
   ```
3. ```javascript
    for (let i=0; i < 4; i++) {
        ... body
    }
    ```

### The "switch" construct 

Switch is used to replace multiple `if` checks and it uses strict equality checks `===` for comparisons. Example : 

```javascript 
let age = prompt('How old are you?', 15);

switch (age) {
    case 15:
     return("Won't work"); // result of prompt is a string, not a number
     
    case '15':
     return("Not it works!");
     break;

    default:
    alert("All other values");
}
```

### Functions 

We have learned 3 types of functions so far: 
1. Function Declaration: 
```javascript
function multiply(a, b) {
    return a * b;
}
```

2. Function Expression:
```javascript
let multiply = function(a, b) {
    return a * b; 
}
```

3. Arrow function:
```javascript
let multiply = (a, b) => a * b;
``` 


## Polyfills 

A polyfill is a browser fallback that allows functionality you expect to work in modern browsers to work in older browsers too. 

### Babel

Babel is a transplier, it rewrites modern JavaScript code into the previous standard so that even the old versions on browsers can read it. 

There are two parts in Babel: 
1. The transplier program, which rewrites the code.
2. The polyfill. For new functions we need to write a special script that implements them. This is where polyfills comes into play, they 'fill in' the gap and add missing implementations. 



## Objects

In JavaScript, objects are used to store keyed collections of various data. Objects can be created with figure brackets `{}` or with `new Object();` statement. For example: 

```javascript
1. let user = {};
2. let user = new Object();
``` 

Objects can have an optional list of properties. A property is a key with a value pair, where they `key` can only by a string but `value` can be anything.
Example: 

```javascript
let user = {
    name: 'Razvan',  // the key is name and value is Razvan
    age: 24,         // the key is age and value is 24
    sex: 'male',
};
```

We can add key and values to objects like so : `user.origin = 'Romania';`  

To add a multiword property we have to use quotes. for example : `"is short": true;`

Dot notation doesn't work for multiword properties. Instead we can use squre bracket notation : `user["is short"] = true;`

We can remove key and value like this : `delete user.name;` 

We can call a property by using object name dot key, for example : `alert(user.age);`


### The "for ...in" loop

To walk over all keys of an object we use the following syntax: 

```javascript
for(key in object) {
    // executes the body for each key among object properties
}
```

*One of the fundamental differences of objects vs primitives is that they are stored and copied "by reference".*

Primitive values are assigned/copied "as a whole value" wheres objects are stored somewhere in the memory and variables have a "reference" to them.



## Garbage collection

All we do in JavaScript takes memory, but memory management is performed automatically and invisibly to us.

### Reachability

Reachability is the main concept of memory management in JavaScript. When a value is not *reachable* anymore (cannot be accessed or used), it is removed by a background process called [Garbage collector](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science)).

Let's have a look at an example to see how an object becomes unreachable: 

```javascript
let user = {
    name: "Razvan"
};  // user has a reference to the object 

user = null; // this modifies the object and now " Razvan " cannot be accessed anymore 
``` 

In the example above, there is no way we can access " Razvan " anymore so the Garbage collector will delete it and free some memory!



## Symbols

So far we have learned that object property keys can only be string type. Now we will learn that it can also be symbol type.

*Symbol* value represents a _unique identifier_ that can be created using `Symbol()` syntax:  

```javascript
let id = Symbol();
```

Symbols can also be given a description, also known as "symbol name". We have to remember tho that even if two or more symbols have the same description, they are different values, for example: 

```javascript
let id1 = Symbol("mat");
let id2 = Symbol("mat");

alert(id1 == id2); // will returne false
```

*Symbols don't auto-convert to string!!!*  To call a symbol, we have to first use the `.toString()` method on it, then it will work. 

### The purpose of a Symbol is to create "hidden" properties of an object.

This comes in handy when we import a library for example and don't want to mess up the code. If we were to use a string value instead of a Symbol, when keys share the same name, they can be overwritten! For example: 

```javascript
let user = { name : "Razvan" };
user.id = "Value inside";

// .. now if someone wants to use "id" for their purpose, this will happen:

user.id = "New value inside"; 

// value of user.id has been overwritten ! 
```

*To use symbol in an object literal, we have to use square brackets, like this:* 

```javascript
let age = Symbol("age");

let user = {
    name: "Razvan",
    [age]: 24  
}; 
```

#### Symbols properties doesn't participate in `for..in` loop. That's because they are hidden.

### Global symbols

There is a way tho access the same property within a symbol, even if we said that every symbol is unique. 

To achieve that, there is a _global symbol registry_ where we can create symbols and access them later, in return having the exact same symbol.

`Symbol.for(key)` is used to create or read a symbol in the registry. If there is already one created, it returns it, otherwise it creates a new one. 

Example:

```javascript

let id = Symbol.for("id");  // if it doesn't exist, it has just been created

let idAgain = Symbol.for("id"); // reads it again

alert( id === idAgain); // true 
``` 



## Object methods, "this"

Functions that are stored in object properties are called "methods". Example: 

```javascript
let user = {
    name: "Razvan",
    age: 24 
    sayHi: function(){
        alert("Hi there");
    }
}; // sayHi property is a function inside an object and it's called method
```


### "this" in methods

*To access the object, a method can use the `this` keyword which value is the object before dot. For example:*

```javascript
let user = {
    name: "Razvan",
    age: 24,

    sayHi() {
        alert(this.name);
    }
};

user.sayHi();  // output will be Razvan 
``` 

In the example above, during the execution of `user.sayHi()`, the value of `this` will be `user`.


### "this" is not bound

In JavaScript, the value of "this" is evaluated during the run-time and it can be anything and used in any function. We can even call the function without an object at all, but the return will be `undefined` : 

```javascript
function sayHi() {
    alert(this);
}
sayHi(); // undefined
``` 

### Arrow functions have no "this" 

When "this" is accessed inside an arrow function, the value it's taken from outside (outer function).



## Object to primitive conversion

To convert an object to a primitive value, we have to use the `ToPrimitive` keyword. There are three variants, also called "hint" to do this : 

1. "string" - when an operation expects a string, for object-to-string conversions. Example : 
```javascript
alert(obj);
// output 

anotherObj[obj] = 33; // using object as a  property key 
```

2. "number" - when an operation expects a number, for object-to-number conversions. Example :
```javascript
let num = Number(obj);  // explicit conversion

let n = +obj; // unary plus 
let delta = date1 + date2; 

let greater = user1 > user 2 // for comparison
```

3. "default" - it rarely happens when operator is " not sure " what type to expect.

Some operands can work with both strings and numbers, like `+`, or when comparing something using `> / <`. For example: 
```javascript
let sum = date1 + date2; // binary + 

if ( user == 1) {...} // obj == string/number/symbol
```

*To do the conversion, JavaScript tries to find and call three object methods: 
1. Call `obj[Symbol.toPrimitive](hint)` if method exists;
2. Otherwise if hint is a `string` - try `obj.toString()` and `obj.valueOf()` whatever exists;
3. Or if hint is `number` or `default` - try `obj.valueOf()` and `obj.toString()` whatever exists. 

### Symbol.toPrimitive
Is a built-in symbol that shoud be used to name the conversion method: 

```javascript
obj[Symbol.toPrimitive] = function(hint) {
    // hint can be "string", "number" or "default" and the return will be a primitive value
}
```

```javascript
let user = {
    name: "Razvan",
    age: 24,

    [Symbol.toPrimitive](hint) {
        alert(`hint: ${hint}`);
        return hint == "string" ? `{name: "${this.name}"}` : this.age;
    }
};
//lets see how the conversion works :
alert(user); // hint: string -> {name: "Razvan"};
alert(+user); // hint: number -> 24;
alert(user + 500); // hint: default -> 524;
```

### toString/valueOf

If there is no `Symbol.toPrimitive` then JS tries to find them in this order: 
- `toString -> valueOf` for "string" hint;
- `valueOf -> toString` otherwise. 

Example: 

```javascript
let user = {
    name: "Razvan",
    age: 24,

    // for hint = "string"
    toString(){
        return this.name;
    },

    // for hint = "number" or "default" 
    valueOf() {
        return this.age;
    }
};

alert(user); // toString -> "Razvan"
alert(+user); // valueOf -> 24
alert(user + 500); // valueOf -> 524
```



## Constructor, operator "new" 

Constructor functions and "new" operator are used when we need to create many similar objects.

### Constructor function

Constructor functions are real functions that start with capital letter first and should only be executed with "new" operator. Example: 

```javascript
function User(name) {
  this.name = name;
  this.isAdmin = false; 
}

let user = new User("Razvan");

alert(user.name); // Jack
alert(user.isAdmin); false
```

Now `let user = new User("Razvan")` from above, does the following things: 
1. Creates an empty object that is assigned to `this`.
2. Executed function body; usually modified `this` and adds new properties to it.
3. The value of `this` is returned.

So, `let user = new User("Razvan")` becomes : 

```javascript
let user = {
    name: "Razvan",
    isAdmin: false
};
```
*The main purpose of constructors is to implement reusable oject creation code.*

### Return from constructors

Usually they don't have a `return` statement. Their job is to write all necessary data into `this` that automatically becomes the result.

If there is a `return` statement, then: 

1. If `return` is called with object, then it is returned insted of `this`. Example:

```javascript
function NewUser() {
 this.name = "Razvan";
 return {name: "Ionut"}; // <-- returns an object
}
alert(new NewUser().name); // <-- returns "Ionut"
```

2. If `return` is called with a primitive, it's ignored. Example:

```javascript
function NewUser() {
    this.name = "Razvan";
    return 8; // finishes the execution, return this
   
   // ... 
}
alert(new NewUser().name); // <-- returns "Razvan"
```

### Methods in constructors

We can add to `this` methods as well, not only properties. Example:

```javascript
function User(name) {
    this.name = name;

    this.sayHello = function() {
        alert("How are you, " + this.name + "?");
    };  // sayHello is the method in this case
}

let michael = new User("Michael");

michael.sayHello(); // How are you, Michael?
```



## Methods of primitives

In JavaScript it is possible to work with primitives as if there were objects, meaning that we can apply methods on them, even if they are not objects.

Primitives are : `string`, `number`, `boolean`, `symbol`, `null` and `undefined`.

An object is created with `{}` and can store multiple values as properties, such as functions. Example: 

```javascript
let user = {
    name: "Razvan",
    sayHello: function() {
        alert("Hi friend!");
    }
};

user.sayHello(); // Hi friend! 
``` 

### A primitive as an object

We can apply methods on primitives for a short period of time. When this happens, the primitive in transformed into an "object wrapper" that provides the extra functionality, after which is destroyed. For example: 

```javascript
let str = "Time to become an object wrapper";
alert(str.toUpperCase()); // TIME TO BECOME AN OBJECT WRAPPER
```
After the method is applied on the primitive, and it is run by the engine, it gets destroyed, meaning that it will go back to it's original form, a primitive. 


*Null and undefined are exception to the rule, they can only be primitive.*



 
