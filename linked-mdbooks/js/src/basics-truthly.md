# Truthly and Falsly

- As well as a type, each value also has an inherent boolean value, generally known as either truthy or falsy. 
- Some of the rules are a little bizarre so understanding the concepts and effect on comparison helps when debugging JavaScript applications.
- The following values are always falsy:
  - `false`
  - `0` (zero)
  - `''` or `""` (empty string)
  - `null`
  - `undefined`
  - `NaN` (e.g. the result of 1/0)
- Everything else is truthy. That includes:
  - `'0'` (a string containing a single zero)
  - `'false'` (a string containing the text “false”)
  - `[]` (an empty array)
  - `{}` (an empty object)
  - `function(){}` (an "empty" function)

### Code Example

The assigned truthly and falsly values can be used to check if a variable exists, but be aware, sometimes a variable exists but has a value assigned that is represented by falsly (for example the Number 0 and any empty String). See example below:

```js
// STRINGS
// truthly (any not empty string)
const strTruthly = "I exist!";
if (strTruthly) {
    console.log("String strTruthly was evaluated truthly");
} else {
    console.log("String strTruthly was evaluated falsly");
}
// falsly
const strFalsly = "";           
if (strFalsly) {
    console.log("String strFalsly was evaluated truthly");
} else {
    console.log("String strFalsly was evaluated falsly");
}

// NUMBERS
// truthly (any number not 0)
const numTruthly = -1;         
if (numTruthly) {
    console.log("Number numTruthly was evaluated truthly");
} else {
    console.log("Number numTruthly was evaluated falsly");
}
// falsly
const numFalsly = 0;
if (numFalsly) {
    console.log("Number numFalsly num was evaluated truthly");
} else {
    console.log("Number numFalsly num was evaluated falsly");
}

```