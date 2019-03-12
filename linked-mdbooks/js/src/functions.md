# Functions

- 4 elements of functions:
  - function keyword `function`
  - function identifier (name) `add`
  - function parameters (inside the `()` brackets)
  - function body (whats inside the `{}` brackets)
- default return value is `undefined` (if not overwritten)
```js
function add(a,b) {
    console.log("Adding " + a + " and " + b);
    return a+b;
}
```

```js
// anonymous function
const x = function (a, b) {return a * b};
console.log(x(2,3));  // 6
```

### Default Parameters (ES06)
```js
// one default parameter
function items(item = "myDefaultItem") {
    console.log(`Item in List: ${defaultName}`);
}
items("pen") // Item in List: pen
items()      // Item in List: myDefaultItem

// multiple parameters
function items(item1 = "pen", item2 = "coffee") {
	console.log(`item1: ${item1}, item2: ${item2}`);
}
items("cup");           // item1: cup, item2: coffee
items("cup", "bag")     // item1: cup, item2: bag
items(undefined, "bag") // item1: pen, item2: bag
items();                // item1: pen, item2: coffee
```

### Arrow Functions (ES06)

```js
const x = (a, b) => {return a * b};
console.log(x(2,3));  // 6
```

**concise body arrow functions**
- functions that take only one parameter don't need to be enclosed in parentheses!
- zero or multiple parameters have to be enclosed in parentheses
- single line blocks do not neet curly braces `{}`!

```js
// one parameter
const increase = input => input++; // be aware, increased value gets returned only!
const squareNum = num => num*num;  // no manipulation on the passed parameter/object

// zero or multiple parameters
const add = (a, b) => a + b;
const pi = () => 3.14;

```




