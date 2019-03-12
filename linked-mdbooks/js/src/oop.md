# OOP

## Object example
```js
var cat = {
    name: "Whiskers",
    legs: 4,
    tails: 1,
    enemies: ["Water", "Dogs"]
};
console.log("my cats name: " + cat.name);    // DOT NOTATION
console.log("my cats name: " + cat["name"])  // BRACKET NOTATION
console.log("nbr of legs: " + cat.legs);     // DOT NOTATION
console.log("nbr of legs: " + cat["legs"];   // BRACKET NOTATION
```

### Add Properties to Object
```js
var myObject = {
	prop1: "something";
}
myObject.prop2 = "something else";              // dot notation
myObject["prop3"] = "a third propertie added";  // bracket notation
delete myObject.prop3;                          // third property deleted!
```

### Check if Property exists
```js
myObject.hasOwnProperty("property"); 
```


### Brackets vs Dot notation
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