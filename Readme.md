# Notes for Javascript

**Navigate to the Topic**

1. [Basis of JS](#basis-of-jS)
2. [The 7 Primitive Data types](#the-7-primitive-data-types)
3. [Operators in JS](#operators-in-js)
4. [Template literals (Template strings)](#template-literals-template-strings)
5. [Conditional Statment ( if-Else )](#conditional-statment--if-else-)
6. [Type Conversion and Coercion](#type-conversion-and-coercion)

## Basis of JS

1. On page Script

```html
<script type="text/javascript">
  ...
</script>
```

2. Include external JS file

```html
<script src="filename.js"></script>
```

3. Output

```js
console.log(a); // write to the browser console
document.write(a); // write to the HTML
alert(a); // output in an alert box
confirm("Really?"); // yes/no dialog, returns true/false depending on user click
prompt("Your age?", "0"); // input dialog. Second argument is the initial value
```

4. Comments

```js
/* Multi line
comment */
// One line
```

5. Functions

```js
function addNumbers(a, b) {
  return a + b;
}
x = addNumbers(1, 2);
```

## The 7 Primitive Data types

- To check the Data type of any Varible / Value

```js
console.log(typeof "ChandraPrakash");
```

- Way of Declaring Variables

```js
var a; // variable
var a = 1,
  b = 2,
  c = a + b; // one line
const PI = 3.14; // constant
let z = "zzz"; // block scope local variable

("use strict"); // Use strict mode to write secure code
x = 1; // Throws an error because variable is not declared
// Creates property on global scope. [Not reccomend to wright Variable without Declaring]
```

1. Number: Floating point numbers -> Used for decimal and integers.

```js
let age = 23;
console.log(typeof age);
```

2. String: Sequence of characters -> Used for text.

```js
let firstName = "ChandraPrakash";
console.log(typeof firstname);
```

3. Boolean: Logical type that can only be true or false -> Used for taking decisiions.

```js
let fullAge = true;
console.log(typeof fullAge);
```

4. Undefined Value by a variables is not yet defind("empty value").

```js
let children;
console.log(typeof children);
```

5. Null: Also means 'empty value'.

```js
let myNull = null;
console.log(typeof myNull);
```

6. Symbol (ES2015): Value that is unquie and cannot be changed _[Not useful for now]_.

7. Biglnt (ES2020): Larger integers than the Number type can hold.

## Operators in JS

- [Arithmetic Operators](#arithmetic-operators)
- [Assignment Operators](#assignment-operators)
- [Comparison Operators](#comparison-operators)
- [Logical Operators](#logical-operators)
- [Ternary Operators](#ternary-operators)

### Arithmetic Operators

```js
console.log(10 + 5); // Addition -> 15
console.log(10 - 5); // Subtraction -> 5
console.log(10 / 2); // Division -> 5
console.log(10 * 4); // Multply -> 40
console.log(7 % 2); // Modulas -> 1
console.log(2 ** 4); // 16
console.log(2++); // Increment -> 3
console.log(2--); // Decrement -> 1
```

- Post and Pre Increment/Decrement

```js
let x = 5;
// x++, it will increase the value of x when the program control goes to the next statement.
// ++x, it will increase the value of x there only

x++; //post-increment, x will be 5 here and 6 in the next line
++x; //pre-increment, x will be 7 here
x--; //post-decrement, x will be 7 here and 6 in the next line
--x; //pre-decrement, x will be 5 here
```

### Assignment Operators

```js
let x = 10 + 5; // Assigns right operand value to the left operand. -> 15
x += 10; // Sum left and right operand and stores in left operand -> 25
x *= 4; // Multiply left and right operand and stores in left operand -> 100
// [ " -= " for Subtraction , " /= " for Division , " %= " for Modulas ]
x++; // 101
x--; // 100
x--; // 99
console.log(x); // 99
```

### Comparison Operators

```js
console.log(40 == 8); // Compares the equality of two operands without considering type.
console.log(40 === 8); // Compares equality of two operands with type.
console.log(40 != 8); // Compares inequality of two operands without considering type.
console.log(40 !== 8); // Compares inequality of two operands with type.
console.log(40 < 8); // Less Than / return true if 40 <> 8
console.log(40 >= 8); // Greater Than equal to / return true if 40 >= 8
console.log(40 <= 8); // Less Than equal to / return true if 40 <>= 8
```

### Logical Operators

```js
let a = 5,
  b = 10;

a != b && a < b; // returns true. // Both Condition should true.
a > b || a == b; // returns false // One Condition should true
a < b || a == b; // returns true
!(a < b); // returns false // Inverse the Solution true <-> false
!(a > b); // returns true
```

### Ternary Operators

The second part (after ? and before :) will be executed if the condition turns out to be true. Suppose, the condition returns false, then the third part (after :) will be executed.

```js
let a = 10,
  b = 5;

var c = a > b ? a : b; // value of c would be 10
var d = a > b ? b : a; // value of d would be 5
```

## Template literals (Template strings)

```js
// Untagged, these create strings:
`string text``string text line 1 
 string text line 2` // Multi line String
`string text ${expression} string text`; // access any veriable by ${variable_name}
```

- Without Template Literals

```js
let a = 5,
  b = 10;
console.log("Fifteen is " + (a + b) + " and \n not " + (2 * a + b) + ".");
// "Fifteen is 15 and
// not 20."
```

- With Template Literals

```js
let a = 5,
  b = 10;
console.log(`Fifteen is ${a + b} and
not ${2 * a + b}.`);
// "Fifteen is 15 and
// not 20."
```

## Conditional Statment ( if-Else )

```js
const age = 19;
if (age >= 18) {
  // logical condition
  status = "Eligible for driving License."; // executed if condition is true
} else {
  // else block is optional
  const yearsLeft = 18 - age;
  status = `Not eligible for driving License. Wait for ${yearsLeft} years`;
  // executed if condition is false
}
```

## Type Conversion and Coercion

- [Type Conversion](#type-conversion) Changing type of the Data explicitly.
- [Type Coercion](#type-coercion) Javascript changing type of the Data implicitly.

### Type Conversion

```js
const inputYear = "1991";
// number() for String to Number
console.log(Number(inputYear), inputYear); // 1991 '1991'
console.log(Number(inputYear) + 18); // 2009

console.log(Number("ChandraPrakash")); // NaN

// String() for Number to String
console.log(String(23)); // 23
```

#### Falsy values

[ 0 , "" , undefined , null , NaN , false ] are false if they are converted to Boolean

```js
console.log(Boolean(0)); // false
console.log(Boolean("")); // false
console.log(Boolean(NaN)); // false
console.log(Boolean(false)); // false
console.log(Boolean(undefined)); // false
console.log(Boolean(null)); // false
```

#### Truely Value

All values are truely if it is not [ 0 , "" , undefined , null , NaN , false ]

### Type Coercion

```js
// 23 Automatically converted to String while logging the String.
// " + " convert number to String
console.log("I am " + 23 + " years old."); // I am 23 years old.

// " - " , " / " , " * "  and also logical operators
// convert String to Number
console.log("23" - "10" - 3); // 10
console.log("23" > "10"); // true

// Example
let n = "1" + 1; // 11
n = n - 1; // 10
console.log(n);
```

## Switch Statment

```js
switch (
  new Date().getDay() // input is current day
) {
  case 6: // if (day == 6)
    text = "Saturday";
    break;
  case 0: // if (day == 0)
    text = "Sunday";
    break;
  default:
    // else...
    text = "Whatever";
}
```
