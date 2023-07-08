### REGEX
```
// all letters and numbers + '-'
let longHand = /[A-Za-z0-9_]/;
let shortHand = /\w/;
let opposite = /\W/; // same as [^A-Za-z0-9_]
let digits = /\d/;   // same as [0-9]

// greedy vs lazy matching
let greedy = /<.*>/;
let lazy = /<.*?>/;

// wildcard period . matches any one character
myRegex.test(myString);  // returns true or false
myString.match(myRegex); // returns the match

// character classes []
let vowelRegex = /[aeiou]/; //matches any one of the vowels
let allRegex = /[a-z0-9]/gi;

// negated character sets ^
// (use ^ outside a character set to match beginning string patterns)
// (use $ at the end of regex to search for ending string patterns)
let negated = /[^0-9aeiou]/gi;

// repeated characters 1 or more times +
let repeatedS = /s+/;
// repeated characters 0 or more times *
let zeroOrMoreS = /s*/;
```
Literal match: ```/hello|hi|hey/```

Flags: 
```
i - ignore case
g - global search

```
