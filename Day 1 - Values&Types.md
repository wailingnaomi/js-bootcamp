### Day 1 

## ECMAScript
ECMAScript is the standard upon which JavaScript is based, and it's often abbreviated to ES.

Naast JavaScript, zijn er ook andere geïmplementeerde talen ECMAScript:

- Actionscript
- JScript

TC39 is de comité van JavaScript.

De leden van TC39 zijn bedrijven die betrokken zijn met JavaScript en browsers als Mozilla, Google, Facebook, Apple, Microsoft, Intel, PayPal etc.

ES.Next is de naam die word genoemd bij de volgende versie van Javascript. Dus nu is het ES2019 en ES.Next is ES2020

## ES5 vs. ES6
```jsx
// Immedeately Invoked Function Expression = IIFE 
function counter(){
	for (var i = 0; i < 10: i++) {
	console.log(i)
	}
}
counter()
console.log('after loop', i)

//
"use strict";
var i = 9999999 ;
function counter(){
	for ( var i = 0; i < 10: i++) {
	console.log(i)
	}
})()
console.log('after loop', i)

// let: only use when you need to change the variable because 
"use strict";
var i = 9999999
for (let i = 0; i <10; i++) {
	console.log(i)
}
console.log('after loop', i)

//const: you schould always use const if you do not absolutely need to change the variable
"use strict";
const x = 1
x = 2 // const kan niet direct opnieuw benoemd worden

"use strict";
const x = {
	y: 5
}
x.y = 6 // zo kan je wel const opnieuw benoemen

```

## Values, types and operators
#Values

**Numbers** 

- Fractional number

```jsx
1.23
```

- Scientific notation 1.23**e**4

```jsx
1.23e4
```

**Arithmetic**

- add **+**
- multiply *****
- subtraction **-**
- division **/**
- remainder/modulo **%**

**Special numbers**

- **infinity** (- 1 = infinity)
- **-infinity**

**Strings**

- "xxxx"

```jsx
"This is a string"
//This is a string
```

- newline **\n** ("This is the first line**\n**And this is the second")

```jsx
"This is the first\nAnd this is the second"
//This is the first
//And this is the second
```

- backslash **\\**

```jsx
"A newline character is written like \"\\n\"."
// A newline character is written like "\n".
```

- concatenates "xx" + "xx"

```jsx
"con" + "cat" + "e" + "nate"
// concatenate
```

- template literals ${x / x}

```jsx
`half of 100 is ${100 / 2}` //let op `
// half of 100 is 50

```

**Unary operators**

- typeof (produces a string value naming the type of the value you give it)

```jsx
console.log(typeof 4.5)
// number
console.log(typeof "x")
// string
```

 **Binary operators**

- > is greater than
- < is less than
- minus operator (can be used both as binary operator and as a unary operator)

```jsx
console.log(-(10-2))
// -8
```

```jsx
Boolean values
```

**Comparison**

- > is greater than
- < is less than

```jsx
console.log(3 > 2)
// true
console.log(3 < 2)
// false
```

- strings (alphabetic ordered)

```jsx
console.log("Aardvark" < "Zoroaster")
// true
```

- >= greater than or equal to
- <= less than or equal to
- == equal to
- != not equal to

```jsx
console.log("Itchy" != "Scratchy")
// true
console.log("Apple" == "Orange")
// false

console.log(NaN == NaN)
// false
```

**Logical operators**

- && and

```jsx
console.log(true && false)
// false
console.log(true && true)
// true
```

- || or

```jsx
console.log(false || true)
// true
console.log(false || false)
// false
```

- ?

```jsx
console.log(true ? 1 : 2);
// 1
console.log(false ? 1 : 2);
// 2
```

**Empty values**

- null
- undefined

**Automatic type conversion**

```jsx
console.log(8 * null)
// 0
console.log("5" - 1)
// 4
console.log("5" + 1)
// 51
console.log("five" * 2)
// NaN
console.log(false == 0)
// true
```

```jsx
console.log(null == undefined);
// true
console.log(null == 0);
// false
```

**Short-circuiting of logical operators**

```jsx
console.log(null || "user")
// user
console.log("Agnes" || "user")
// Agnes
```

## Conventions
If a variable will not be reassigned, prefer `const` otherwise use `let`

use strict equality and inequality, for example: `===` and `!==`

use shortcuts for boolean tests `x` and `!x`, not `x === true` and `x === false`

use template literals `${xxx}`

```jsx
let myName = 'Naomi';
console.log(`Hi! I'm ${myName}!`);
```

when inserting strings into DOM nodes, use `Node.textContent`, not `Element.innerHTML`

add items to an array with `push()`

```jsx
const pets =[];
pets.push('cat');
```