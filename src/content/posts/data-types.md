---
title: Data Types in JavaScript
published: 2025-03-04
tags: ["ZeroToDev", "JavaScript"]
category: DevNotes
draft: true
---

# Data Types

OVERVIEW

7 Types of Data

1. NUMBER
2. BIGINT
3. STRING
4. BOOLEAN
5. NULL VALUE
6. UNDEFINED VALUE
7. OBJECTS AND SYMBOLS

Primitive Types:

- Number

- BigInt

- String

- Boolean

- Undefined

- Null

- Symbol

Non-Primitive Type:

- Object


So far i learn a lot of different data types, they are mostly from odin-project and google documentation where i try to understand them. In order to understand it more (making sure i understand it) i will make this article but in my own words, in a sense that if i can explain it by myself then atleast i understand half of it, but this article will also set as a reminder for me in case i need to study it again.

Note: I will put easy referal links in case i want to study it again.

TYPEOF OPERATOR is used to determine the type of a value, this can be useful if you try to check what type of data you want to see.

You can use TYPEOF to check if you want.

```js

console.log(typeof 123);          // "number"
console.log(typeof "hello");      // "string"
console.log(typeof true);         // "boolean"
console.log(typeof undefined);    // "undefined"
console.log(typeof null);         // "object"
console.log(typeof Symbol());     // "symbol"
console.log(typeof {});           // "object"
console.log(typeof function(){}); // "function"

```


## 1. NUMBER

Number type can represent both integer and floating point numbers, for example:

```js

let n = 123

n = 12.345

```
There are many operations for numbers, for e.g

- Multiplication (*)

- Division (/)

- Addition (+)

- Subtraction (-)

In Number Type data there are also special numeric values, they are Infinity, -Infinity, and NaN

- Infinity: Represents infinty from maths that has value bigger than any number

- -Infinity: The value is the opposing of Infinity, which has negative value bigger than any number

e.g 

```js

alert( 1 / 0 ) // Result will be Infinity

OR

alert( Infinity ) // Result will be Infinity

OR

console.log(-1 / 0); // Output: -Infinity

```

- NaN: NaN gives a sign that there is a computational error, because the result of an operation is wrong or undefined

e.g

```js

alert ( "Not a number" / 2 ) // The result will be NaN because the operation is invalid or undefined

```

Though JavaScript do provides method to convert string to numbers, for e.g

```js

console.log(Number("123")); // Output: 123
console.log(Number("123abc")); // Output: NaN

console.log(parseInt("123abc")); // Output: 123
console.log(parseFloat("123.45abc")); // Output: 123.45


```

## 2. BIGINT


BigInt is a special type of integer in JavaScript that can store large integers beyond the safe limit of the regular Number type (which is ±(2^53 - 1)). Commonly used in data that requires extremely large numbers like cryptography, precise calculations, and timestamps in nanoseconds or microseconds

- To create a BigInt, simply use n at the end of a number
- Mathematical operations with BigInt can be performed with other BigInt, not with regular numbers to avoid errors


```js

// the "n" at the end means it's a BigInt
const bigInt = 1234567890123456789012345678901234567890n;

// Regular number has limitations
console.log(Number.MAX_SAFE_INTEGER); 
// Output: 9007199254740991

// Exceeding the safe limit with regular number
console.log(9007199254740991 + 1); 
// Output: 9007199254740992 (Incorrect due to precision loss)

```