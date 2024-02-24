
### String methods:
- (slice vs substring)[https://stackoverflow.com/questions/2243824/what-is-the-difference-between-string-slice-and-string-substring]
```
str.length
str[0]
let string = "" + 23;
number.toString();
Number(string);

// split str into array of substrings separated by separator
let arr = str.split("");

// reverse str
str.split("").reverse().join("")
[...str].reverse().join("")

str.slice(start, end);
```
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

// use indexOf() to check position of ele in arr; doesn't exist returns -1
let index = arr.indexOf(ele);

// use every(), forEach(), map() to iterate through elements in an array
// use reverse() to reverse array

// use map(callbackFn)
// use filter(callbackFn)
const arr = [1,2,3,4,5]

arr.filter(bigEnough);

const bigEnough = (arrElement, index, array) => {
  return arrElement > 3;
}
```
---
### Objects 
- collections of key-value (property-data) pairs
- does not maintain an ordering to stored keys like arrays do
```
const obj = {
  123: "",
  prop1: "",
  prop 1: ""
}
```
Access properties:
```
// dot notation
let a = obj.prop1;

// bracket notation
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
// or
return propName in obj;

// This doesn't work! Argument needs to be a variable or in ""
return obj.hasOwnProperty(prop1);
```

Iterate through keys in obj:
```
for (const user in allUsers) {
  console.log(user, allUsers[user]);
}
```

Get array of properties from obj:
```
let arr = Object.keys(obj);
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
