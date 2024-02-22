### OOP

### Arrow Function (ES6):
- **this** value in arrow functions is determined based on the lexical scope (ability to access variables from its parent scope)
  
[understanding arrow functions](https://www.digitalocean.com/community/tutorials/understanding-arrow-functions-in-javascript)

[this keyword explanation](https://www.digitalocean.com/community/conceptual-articles/understanding-this-bind-call-and-apply-in-javascript)

[arrow function doc](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
```
const myFunc = () => {
  let a = 123;
  return a;
}
const myFunc = () => 123;

// set default value to parameters
const myFunc = (name="anon") => "hi, " + name;

// using the rest parameter for arbituary number of arguments
const myFunc = (...args) => args.length;

// the spread operator expands iterables in places where zero or more arguments are expected (into comma-separated list)
const nums = [1,2,3];
console.log(sum(...nums));
console.log(sum.apply(null, nums));

// Destructuring statement
const { prop1, prop2 } = obj;
// Assign new varialbes names
const { prop1: newProp1, prop2: newProp2 } = obj;

// Destructure Arrays 
const [a, b, , d] = [d, c, b, a];  // a=d, b=c, d=a

// w/ the rest operator
const [,, ...removeFirstTwo] = [1, 2, 3, 4, 5, 7];  // removeFirstTwo = [3, 4, 5, 7]
```
```
// create strings with Template Literals
const greeting = `Hello, my name is ${person.name}!
I am ${person.age} years old.`;

```
---
### Random
- var declares a variable globally or locally to an entire function regardless of block scope
- let has the additional feature that it is declared with block scope (only available in the block)
- const doesn't prevent mutation, Object.freeze() does
```
// generate random number from 0 to 99
Math.floor(Math.random() * 100);
// generate raondom number from min to max inclusive
Math.floor(Math.random() * (max - min + 1)) + min
//
parseInt(str, radix);
// conditional operator (a ? b : c)
```
- the equality operator (==) performs type coercions
- the strict equality operator (===) does not perform type coercions

Export / Import
```
<script type="module" src="index.js"></script>
export { func0, func1 };
import { func0, func1 } from './index.js';
import * as funcs from "./index.js";

export defalut function func0() {}
// or export defalut func0;
import anyName from "./index.js";
```
Promise
```
const p = new Promise((resolve, reject) => {
  if(condition) {
    resolve();
  }
  else {
    reject();
  }
});
// then is executed after resolve is called
// result comes from the argument given to the resolve method
p.then(result => {
});
// catch is executed after reject is called
// error comes from the argument given to the reject method
p.catch(error => {
});
```


---

### Function:
- closures
- when a function is declared inside another function,
- the inner function can access variables in the scope of the outer function even after the outer function finishes executing (lexical scope)
- useful for creating private variables and functions
```
function sum(a, b) {
  console.log("Hello World");
  return a + b;
}
============================>
const sum = function (a,b) {
  return a + b;
}
============================>
const sum = (a,b) => {
  return a + b;
}
============================>
// self-invoking function
((a,b) => a + b; )(2,3);
```
---

