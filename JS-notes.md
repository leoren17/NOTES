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
```
Array methods:
```
let myArray = [];                       // []
myArray.push(["ele0", "ele1"]);         // ["ele0", "ele1"]
myArray.unshift("new0");                // ["new0", "ele0", "ele1"]
let lastElement = myArray.pop();        // ["new0", "ele0"]  // lastElement = "ele1"
let firstElement = myArray.shift();     // ["ele0"]          // firstElement = "new0"
myArray.unshift(firstElement);          // ["new0", "ele0"]
```
Function:
```
function sum(a, b) {
  console.log("Hello World");
  return a + b;
}
let three = sum(1, 2);  
```
Queue:
Arrow Function:
```
```
