# Build In Object Methods

see [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) from mozilla for further dokumentation.

### **`Object.keys()`**

```js
const obj = {
  a: 'somestring',
  b: 42,
  c: false
};

console.log(Object.keys(obj));
// expected output: Array ["a", "b", "c"]
```

### **`Object.entries()`**

```js
const obj = {
  a: 'somestring',
  b: 42,
  c: false
};

console.log(Object.entries(obj));
// expected output: 
// [ Array ["a", 'somestring'], Array ["b", 42], Array ["c", false] ]

// Iterating through Objects:
Object.entries(obj).forEach(([key, value]) => {
    console.log(`${key}: ${value}`);
});
```

### **`Object.assign()`**

```js
// reassigns "key: value" pairs of target object
// input: one or multiple source objects
// if key exists in target: will be reassigned
// if key does not exist in target: will be created
const target = { a: 1, b: 2 };
const source1 = { b: 5, c: 6 };
const source2 = { d: -1 };

// returns new Object...
const returnedObj = Object.assign(target, source1, source2);
console.log(returnedObj);
// expected output: Object { a:1, b:5, c:6, d:-1}

// ...but also manipulates original object!!
console.log(target);
// expected output: Object { a:1, b:5, c:6, d:-1}
```

### **`Object.freeze()`**

- does not work in chrome...!
- create immutable (read only objects)

```js
"use strict"; // throws errors when bugs in code

const obj = Object.freeze({
    a: 42
});

obj.a = 33;
// Throws an error in strict mode -> read-only!

console.log(obj.a);
// expected output: 42 -> initial assignment
```


