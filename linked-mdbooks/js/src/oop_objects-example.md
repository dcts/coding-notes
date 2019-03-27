# Object Example (with Getters/Setters and Methods)

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

cat.age = 12; // setter method (looks like assigning a value)
              // -> but its using the set method to assign 
              //    the variable _age!
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
