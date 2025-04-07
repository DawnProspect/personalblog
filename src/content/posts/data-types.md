---
title: Data Types in JavaScript
published: 2025-04-07
tags: ["ZeroToDev", "JavaScript"]
category: DevNotes
draft: false
---

# Data Types


Learn about all data types in JavaScript.


## OVERVIEW OF THIS ARTICLE.

8 Types of Data

1. NUMBER
2. BIGINT
3. STRING
4. BOOLEAN
5. NULL VALUE
6. UNDEFINED VALUE
7. OBJECT
8. SYMBOLS

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
There are many operations for numbers, for example:

- Multiplication (*)

- Division (/)

- Addition (+)

- Subtraction (-)

In Number Type data there are also special numeric values, they are Infinity, -Infinity, and NaN

- Infinity: Represents infinty from maths that has value bigger than any number

- -Infinity: The value is the opposing of Infinity, which has negative value bigger than any number

Example:

```js

alert( 1 / 0 ) // Result will be Infinity

OR

alert( Infinity ) // Result will be Infinity

OR

console.log(-1 / 0); // Output: -Infinity

```

- NaN: NaN gives a sign that there is a computational error, because the result of an operation is wrong or undefined

Example:

```js

alert ( "Not a number" / 2 ) // The result will be NaN because the operation is invalid or undefined

```

Though JavaScript do provides method to convert string to numbers, for example:

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

## 3. STRING

A string is a data type that represents text.

Example:

```js

const string = "the revolution will not be televised"
console.log(string)

```

You can also use 3 different ticks for string

```js

'the revolution will not be televised' // single quotes

"the revolution will not be televised" // double quotes

`the revolution will not be televised` // backtics

```

Though you are not allowed to use different ticks

```js

const badQuotes = 'This is not allowed!"

```

for string there is special case when you use backtick, you can use template literal where it is almost the same as normal string but have special property where you can embed values in that string

> Using backticks ` allows you to embed variables or expressions directly into strings. This is called template literals:

for example

```js

const name = "Ghost"
const greeting = `Hello, ${name}`
console.log(greeting, "<< Example embedding in JavaScript")

// OR

const one = "Hello, ";
const two = "how are you?";
const joined = `${one}${two}`;
console.log(joined); // "Hello, how are you?"

// OR

const car = "toyota yaris"
const score = 9
const highestScore = 10

const output = `I like the car called ${car}. I gave it a score of ${(score / highestScore) * 100}%`

console.log(output,"contoh output JavaScript Expressions")

```

You can use line breaks as well if the line is too long (Multiline Strings)

> Backticks also allow multiline strings without needing escape characters:

```js

const myNewLine = `One day you finally knew 
what you had to do, and began,`;

console.log(myNewLine, "<< Contoh output newLine")

// OR

const newline = "One day you finally knew\nwhat you had to do, and began,";
console.log(newline);

```

So then, how do you use quotes in strings? you can do it by doing this

```js

const exampleQuotes1 = `He said "I think this is fine"`
const exampleQuotes2 = 'He said "I think this is fine"'


```

You can also Add number type data + strings, though it will turn into strings


```js

const myString = 123
const word = "Front "

// the result: "Front 123"
console.log(word + myString)

```


## 4. BOOLEAN

Boolean type has two values and they are tru and false, true means its correct, yes, or active. While false is incorrect, no, or inactive.

Example:

```js
let nameFieldChecked = true // this meant field called name is already checked, hence it has value true

let ageFieldChecked = false // this meant field called age has not been checked yet, so its considered false

```

Boolean also usually used for comparisons, logic, decision-making, and condition checking.

```js

let isGreater = 4 > 1

console.log(isGreater) // the result should be true because 4 is bigger than 1

console.log(10 === 10); // true

console.log(5 < 3);     // false

```


## 5. NULL

Null is a special value that represents nothing, empty, or unknown. it is a primitive type but unlike other types, it has only one possible value and that is null.

Mostly often used to intentionally clear a variable or show a value is unknown or missing in purpose.

Example:

```js

let age = null

// age will be null

```

6. UNDEFINED VALUE
7. OBJECTS AND SYMBOLS

## 6. UNDEFINED VALUE

Undefined value is almost the same as null because undefined does not belong to anything and it is also representing not assigned, which means the variable is present or exists but not assigned. Easiest way to understand it is undefined means “no value has been assigned.” Which is why it is called undefined.

Example:

```js

let age;

alert(age) 

// the result is going to be undefined
// This means the variable age exists, but we haven't given it a value yet, so JavaScript says it's undefined.

```

### (Small Notes) Then what is the difference between null and undefined?

a. Meaning

Null: Value is intentionally empty.
Undefined: Value is not assigned (yet)

b. Set By

Null: Set by developer (manually)
Undefined: JavaScript (automatically)



## 7. OBJECTS

An Object is a special type in JavaScript used to store multiple values in a single variable, instead of just one value like a string or number, objects can store a collection of key-values pairs, if you want easy example, think objects like a box of labeled data where objects is like a box and data stores inside it is like belongings stored inside that box.

Example of objects

```js

let person = {
    name: "Silvia",
    age: 30,
    isStudent: false
};

console.log(person.name); // Output: Silvia

```

Explanation:

object called "person" stores multiple pieces of data

- name is a key with value "Silvia"
- age is a key with value 30
- isStudent is a key with value false

Simple important note: Objects are used when you want to group related data together.

## 8. SYMBOLS

A Symbol is special and unique type to create unique identifiers for object properties, even if two symbols have the same description, they are not equal.

Example

```js

let id1 = Symbol("id");
let id2 = Symbol("id");

console.log(id1 === id2); // false


```

Symbols are mostly used when you want to make sure a property in an object won’t accidentally overwrite another — especially in large projects or libraries.


Example:

```js

let userId = Symbol("id");

let user = {
    name: "Reza",
    [userId]: 123 // symbol property
};

console.log(user[userId]); // 123

```


## Good references/resources to study data types

> https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Strings#numbers_vs._strings
>
> https://javascript.info/types
>
> https://www.petanikode.com/javascript-variabel/
>
> https://www.w3schools.com/js/js_datatypes.asp
>
> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Data_structures