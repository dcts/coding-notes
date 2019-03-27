# For-Each

```js
let arr = [1,2,3,4,"hello",6];
for (let a of arr) {
    console.log(a);
}
```

- not limited to arrays. Also looping through objects possible!
- for arrays you can also use the `forEach()` method ([see "Iterator: .forEach()"](arrays.md#array-functions))

### Looping through Objects

```js
myObject = {
	name: "arthur",
	age: 78
}

// loop through object and display all property names and values
for (let props in myObject) {
  console.log(`${props}: ${myObject[props]}`)
};
// outputs:   
//   name: arthur  
//   age: 78
```

