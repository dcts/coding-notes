# Array Example

```js
// initialize and assign empty array
var myArray = [] 

// fill array
myArray     = ["stringinput", 23, "hey"];

// initialize and fill in one step
var matrix = [[1,2,3],
              [4,5,6],
              [7,8,9]];

// ARRAY LENGTH
myArray.length            // no curly braces! (same syntax as with strings)

// LAST ELEMENT
myArray.push(content);	  // pushing to end of array
myArray.pop()             // takes away last element and returns it

// FIRST ELEMENT
myArray.unshift(content); // pushing to beginning of array
myArray.shift();          // takes away first element and returns it
```

**Important**: Arrays mutated inside of a function will keep that change even outside the function
```js
function myFunc (arr) {
    arr.push("pushed element!"); // change also visible outside function!
}
```

### Nested Arrays (Matrices)

```js
const matrix = [[1,2],[3,4]]; // matrix

// call matrix
console.log(matrix[1][0]); // row:1, col:0 -> 3
```
