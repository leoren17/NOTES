
### Array methods:
```
let myArray = [];                       // []
myArray.push(["ele0", "ele1"]);         // ["ele0", "ele1"]
myArray.unshift("new0");                // ["new0", "ele0", "ele1"]
let lastElement = myArray.pop();        // ["new0", "ele0"]  // lastElement = "ele1"
let firstElement = myArray.shift();     // ["ele0"]          // firstElement = "new0"

const newArr = myArray.concat(myArray);

// use splice(start, deleteCount, item0, ...) to remove and insert consecutive elements 
const arr = [0,1,2,3,4,5];
let newArr = arr.splice(3, 3);          // [3,4,5]
arr.splice(0,0,{},{},{});               // [{},{},{},3,4,5]

// use slice(start, end) to copy elements without modifying the original
const arr = [0,1,2,3,4,5]
arr = arr.slice(2,3);                   // [2]

// use toString() and join("seperator") to return a string representation
let text = arr.join(" and ");

// use the spread operator (...) to combine arrays
let newArr = [1, 2, ...oldArr, 9, 10];

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
Setters and Getters:
```
class Object {
  constructor(prop1) {
    this._prop1 = prop1;
  }

  get prop1() {
    return this._prop1;
  }

  set prop1(updatedProp1) {
    this._prop1 = updatedProp1;
  }
}

const obj = new Object("p1");
console.log(obj.prop1);
obj.prop1 = "newP1";
console.log(obj.prop1);
```
