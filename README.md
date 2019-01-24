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
