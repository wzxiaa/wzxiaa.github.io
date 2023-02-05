---
title: JavaScript Data Types and Variables
date: 2021-01-14 22:38:20
tags: JavaScript
category:
	- JavaScript Road Map
---

JavaScript is a ***dynamic programming language*** which means that operations otherwise done at the compile-time can be done at run-time. JavaScript is a ***loosely typed*** language as well. Variables in JavaScript are not directly associated with any particular value type and any variables can be assigned values of ***all types***. 

In JavaScript, a variable may store two types of value: `primitive` and `reference`.

- Primitive Data Types characteristics:
  - Stored directly in the location the variable accesses
  - Size of the primitive value is fixed and stored on the stack
  - Accessed by value (manipulate the actual value stored in the variable)
- Reference Data Types characteristics:
  - Accessed by reference
  - Size of reference value is dynamic and objects are stored on the heap
  - A pointer to a location in memory

<!-- more -->

### Primitives

**`Number`** for numbers of any kind: integer or floating-point. Integers are limited by $\pm (2^{53}-1)$. Special number includes: `Infinity`, `-Infinity` and `NaN`. 

**`BigInt`** is for integer number of arbitrary length

**`String`** for strings. A String may have zero or more characters, there's no separate single character type.

1. Double quotes : `"Hello"`
2. Single quotes : `'Hello'`
3. Backticks :  `Hellow`

```javascript
let name = "John";
alert(`Hello, ${name}!` ); // Hellow, John!
```

**`Boolean`** for `true` or `false`

**`null`** for unknown values - a standalone type that has a single value `null`. 

**`undefined`** for unassigned values - a standalone type that has a single value. If a variable is declared, but not assigned, then its value is undefined.

**`Symbol`** is used to create unique identifiers for objects.

### Reference

**`Object`** used to store collections of data and more complex entities. It can includes:

- Arrays, Object literals, Functions, Dates, ... etc

***

### Type Conversion (Explicit)

Convert Number to String:

```javascript
val = String(555);

console.log(val); // 555
console.log(typeof val) // string
console.log(val.length) // 3
```

Convert Boolean to String:

```javascript
val = String(true);

console.log(val); // true
console.log(typeof val) // string
console.log(val.length) // 4
```

Convert Date to String:

```javascript
val = String(new Date());

console.log(val); // Fri Jan 15 2021 13:40:08 GMT-0500 (Eastern Standard Time)
console.log(typeof val) // string
console.log(val.length) // 57
```

Convert Array to String:

```javascript
val = String([1,2,3,4,5]);

console.log(val); // 1,2,3,4,5
console.log(typeof val) // string
console.log(val.length) // 9
```

***toString()*** method:

```javascript
val = (5).toString();

console.log(val); // 5
console.log(typeof val) // string
console.log(val.length) // 1
```

***

Convert String to Number:

```javascript
val = Number('5');

console.log(val); // 5
console.log(typeof val) // number
console.log(val.toFixed()) // 5
```

Convert Boolean to Number:

```javascript
val = Number(true);

console.log(val); // 1 for true, 0 for false and null
console.log(typeof val) // number
console.log(val.toFixed()) // 1
```

Convert Date to Number:

```javascript
val = Number(true);

console.log(val); // 1 for true, 0 for false and null
console.log(typeof val) // number
console.log(val.toFixed()) // 1
```

Convert Non-numeric value to Number:

```javascript
val = Number(new Date());

console.log(val); // 1610736853895
console.log(typeof val) // number
```

***parseInt()*** and ***parseFloat()*** method:

```javascript
val = parseInt('100.30');

console.log(val); // 100
console.log(typeof val) // number
console.log(val.toFixed()) // 100

val = parseFloat('100.31');

console.log(val); // 100.31
console.log(typeof val) // number
console.log(val.toFixed()) // 100.3100
```

### Type Coercion (Implicit)

Type coercion is the process of automatic or implicit conversion of values from one data type to another. 



 







