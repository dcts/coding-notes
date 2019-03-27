# Brackets vs Dot Notation

```js
// bracket notation allows the use of characters 
// that can't be used with dot notation:
var foo = myForm.foo[];     // incorrect syntax
var foo = myForm["foo[]"];  // correct syntax

// Secondly, bracket notation is useful when dealing
// with property names which vary in a predictable way:
for (var i = 0; i < 10; i++) {
    someFunction(myForm["myControlNumber" + i]);
}
```
