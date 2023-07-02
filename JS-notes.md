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
---
### Objects 
```
const obj = {
  123: "",
  prop1: "",
  prop 1: ""
}
```
Access properties:
```
let a = obj.prop1;

let propName = "prop 1";
let b = obj[propName];
// or
let b = obj["prop 1"];

// This doesn't work! Don't use dot access for variables
let b = obj.propName;
```
Delete properties: 
```
let propName = "prop 1";
delete obj.prop1;
delete obj[prop 1];
```

Lookup if property exists: 
```
let propName = "prop1";
return obj.hasOwnProperty(propName);

// This doesn't work! Argument needs to be in ""
return obj.hasOwnProperty(prop1);
```


---
- the equality operator (==) performs type coercions
- the strict equality operator (===) does not perform type coercions
```
str.length
str[0]
ReactDOM.render(JSX, document.getElementById('root'))
let string = "" + 23;
```
Array methods:
```
let myArray = [];                       // []
myArray.push(["ele0", "ele1"]);         // ["ele0", "ele1"]
myArray.unshift("new0");                // ["new0", "ele0", "ele1"]
let lastElement = myArray.pop();        // ["new0", "ele0"]  // lastElement = "ele1"
let firstElement = myArray.shift();     // ["ele0"]          // firstElement = "new0"
myArray.unshift(firstElement);          // ["new0", "ele0"]

const newArr = myArray.concat(myArray);
```
Function:
```
function sum(a, b) {
  console.log("Hello World");
  return a + b;
}
let three = sum(1, 2);  
```
---
Arrow Function (ES6):
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
