---
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
