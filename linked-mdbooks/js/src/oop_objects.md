# Objects

## Object example (inkl. Methods / Getters / Setters)
```js
// OBJECT LITERAL (= variable thats holding an object)
let myObjectLiteral = {};  // empty object

// CAT OBJECT EXAMPLE
var cat = {               // underscore indicates private fields
    _name: "Whiskers",    // only an agreed form of syntax
    _age: 5,              // -> js doesn't treat them differently!
                          
    // OBJECT METHODS (ES06 style)
    makeSound () {
        console.log("miau");
    },                          // dont forget comma
	attack () {                 
        console.log("grrr!");
    },

    /* OBJECT METHODS old style:
    * makeSound: function() {
    *   console.log("miau");
    * },
    * attac: function() {
    *   console.log("grrr!");
    * },
    */ 

    // GETTERS (starting with keyword "get")
    get name() {
    	return this._name;
    }, 
   	get age() {
   		return this._age;
	},

	// SETTERS (starting with keyword "set")
    set name(newName) {
    	this._name = newNane; 
   	}, 
	set age(newAge) {
		this._age = newAge;
	}                         // no comma at end                           
};
console.log("my cats name: " + cat.name);    // DOT NOTATION
console.log("my cats name: " + cat["name"])  // BRACKET NOTATION
console.log("nbr of legs: " + cat.legs);     // DOT NOTATION
console.log("nbr of legs: " + cat["legs"];   // BRACKET NOTATION

// USING OBJECT METHODS
cat.makeSound();
cat.attack();

cat.age();  // getter method
cat.age;    // shortform!
```

to see how you can loop through objects check out the section [Loops - ForEach](loops-foreach.md).


### Add Properties to Object
```js
// with the assign operator (=) we can create new object-properties
// if the propery name is already existant, it gets overriden.
var myObject = {
	prop1: "something";
}
myObject.prop2 = "something else";            // create new prop (dot notation)
myObject["prop3"] = "a third property added"; // create new prop (bracket notation)
myObject.prop1 = "another change";            // updates / overrides prop2!
delete myObject.prop3;                        // third property deleted!

// Check if Property exists
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


### Const Object
Objects initialized with `const` can be mutated (add and remove properties as well as assign new propery-values). But they can't be reasigned.

```js
const cat = {
	id: 1,
	name: "kitty",
	age: 23
};
// SOME ACTIONS 
cat.age = 24;          // works, updates propery-value
cat.gender = "female"; // works, creates new property
delete cat.id;         // works, deleted ip-property
cat = {}               // error! const can't be reassigned!
```


