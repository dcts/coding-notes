# Const Objects

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

