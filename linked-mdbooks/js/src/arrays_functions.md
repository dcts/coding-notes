# Array Functions

- Functions
  - [.sort()](arrays_functions.md#sort): sort an array
  - [.concat()](arrays_functions.md#concat): merge two arrays
  - [.slice()](arrays_functions.md#slice): "substring" for arrays
  - [.splice()](arrays_functions.md#splice): remove and inject elements
- Iterators
  - [.forEach()](arrays_functions.md#foreach): do for each element
  - [.map()](arrays_functions.md#map): do for each element and return new array
  - [.filter()](arrays_functions.md#filter): return filtered array
  - [.findIndex()](arrays_functions.md#findindex): find first index where a condition is met
  - [.reduce()](arrays_functions.md#reduce): operates with 2 elements of array in each step
  - [.some()](arrays_functions.md#some): returns T or F if some elements 
  - [.every()](arrays_functions.md#every)

## `.sort()`
```js
// sorts array (only alphabetically, numbers wont sort numerically)
// manipulates the array itself (object manipulation)
// arraymanipulation works also on const arrays
["a","f","c"].sort(); // returns ["a", "c", "f"]
[5,43,1].sort();      // returns [1,43,5] (!!!)
.sort()
```

## `.concat()`
```js
// does NOT manipulate original array
// returns new array!
[1,2,3].concat([4,5,6]) // returns [1,2,3,4,5,6]
```

## `.slice()`
```js
// like a substring, just with arrays
// returns a new array!
.slice(firstIndex)            // lastIndex automatically the end!
.slice(firstIndex, lastIndex) // first index included, last index excluded
// EXAMPLES
const array = [0,1,2,3,4];
array.slice(2);  // returns [2,3,4] -> subarray starting at index 2
array.slice(2,4) // returns [2,3]   -> last index not included
array.slice(0,2) // returns [0,1]   -> first 2 elements of array
array.slice(-2)  // returns [3,4]   -> last 2 elements of array
```

## `.splice()`
```js
// delets some elements and injects n new ones
// manipulates the object and returns removed elements as new array
.splice(startingIndex, deleteCount, item1, item2, item3, ..., item n)
// EXAMPLEX
const array = [0,1,2,3,4];
array.splice(0,2, -1,0,1); // first two elements are removed [0,1]
                           // injected elements are [-1,0,1] 
                           // array after functioncall: [-1,0,1,2,3,4]
                           // removed elements [0,1] are returned as new array

```

## `.forEach()`
```js
// does NOT manipulate original array
// not returning anything
const artists = ['Picasso', 'Kahlo', 'Matisse', 'Utamaro'];
artists.forEach(artist => {
    console.log(`${artist} is one of my favorite artists.`);
});
```

## `.map()`
```js
// does NOT manipulate original array
// returns new array!
const numbers = [1, 2, 3, 4, 5];
const squareNumbers = numbers.map(number => {
  return number * number;
});
```

## `.filter()`
```js
// does NOT manipulate original array
// returns new array!
array.filter(element => { 
  return (condition);      // returns the array element when truthy!
})
// EXAMPLE
const things = ['desk', 'chair', 5, 'backpack', 3.14, 100];
const onlyNumbers = things.filter(thing => {
  return typeof thing === 'number';
});
```

## `.findIndex()`
```js
// finds FIRST index where given condition is true
// does not manipulate original array
// returns one number (index)
const numbers = [99, 25, 100, 78, 5, 9]; 
const biggerThan100 = numbers.findIndex(num => {
  return num > 100;
});
// returns 2 (because element with index 2 is the first one to be >100)
```

## `.reduce()`
```js
const array1 = [1, 2, 3, 4];
const reducer = (inp1, inp2, inp3, inp4) => inp1 + inp2;
// inp1 = accumulator -> variable that is assigned 0 at start
//                       and is passed over to each iteration
// inp2 = currentValue (of the current element)
// inp3 = currentIndex (of the array)
// inp4 = array (full array is passed)

// 1 + 2 + 3 + 4
console.log(array1.reduce(reducer));
// expected output: 10

// 5 + 1 + 2 + 3 + 4
console.log(array1.reduce(reducer, 5));  // 5 is the second argument of .reduce()
// expected output: 15                   // -> assigns start value for accumulator
```

## `.some()`
```js
// returns true or false
// no object manipulation
// checks if a condition is true for at least one element of the array!
var array = [1, 2, 3, 4, 5];
array.some(element => {
  return element >3;
});
// expected output: true (because 2 elements are bigger than 5)
```

## `.every()`
```js
// returns true or false
// no object manipulation
// checks if a condition is true for ALL elements of the array!
var array = [1, 2, 3, 4, 5];
array.every(element => {
  return element >5;
});
// expected output: false (because not all elements are bigger than 5)
```
