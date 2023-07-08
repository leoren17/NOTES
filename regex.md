### REGEX
```
// search and replace
"Ren Leo".replace(/(\w+)\s(\w+)/, '$2 $1');
// remove beginning and ending whitespace
let wsRegex = /^\s*|\s*$/g; 
let result = "  hi  ".replace(wsRegex,""); 

// capture groups
let repeatRegex = /(\w+) \1 \1/;

// Lookahead (?=... and ?!=...)
let pwRegex = /(?=\w{6})(?=\D*\d{2})/; // greater than 5 characters and have 2 consecutive digits

// ? checks for 0 or more preceding element (previous element is optional)
let reColor = /colou?r/;

// all letters and numbers (\w)
let longHand = /[A-Za-z0-9_]/;
let shortHand = /\w/;
let opposite = /\W/; // same as [^A-Za-z0-9_]

// all digits
let digits = /\d/;   // same as [0-9]

// whitespace
let whitespace = /\s/;
let sameAs = /[ \r\t\f\n\v]/;

// greedy vs lazy matching
let greedy = /<.*>/; // defalut; longest match
let lazy = /<.*?>/;  // shortest match (for .*)

// wildcard period . matches any one character
myRegex.test(myString);  // returns true or false
myString.match(myRegex); // returns the matches in an array []

// character classes [] (match single character with multiple possibilities)
let vowelRegex = /[aeiou]/; //matches any one of the vowels
let allRegex = /[a-z0-9]/gi;

// negated character sets ^
// (use ^ outside a character set to match beginning string patterns)
// (use $ at the end of regex to search for ending string patterns)
let negated = /[^0-9aeiou]/gi;

// repeated characters 1 or more times +
let oneOrMoreS = /s+/;
// repeated characters 0 or more times *
let zeroOrMoreS = /s*/;
// repeated characters within a certain range
let threeToFiveS = /s{3,5}/;
```
Literal match: ```/hello|hi|hey/```

Flags: 
```
i - ignore case
g - global search

```
