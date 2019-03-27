# Functions

### With Keyword `function`

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

### Function Expression / Anonymous Functions
- anonymous functions -> have no function identifier (no name)
- can be stored in variables!
- use case: to pass functions into other functions we can use function expressions
```js
const x = function (a, b) {return a * b};
console.log(x(2,3));  // 6
```

### Self-Evoking Functions
- anonymous function is created and instead of stored in a variable directly evoked (called)
```js
(function(a,b) {    // anonymous function
	return a+b      // adds 2 numbers
})(1,2);            // enclosed in () makes it self-evoking. 
                    // last () are here to pass parameters
```

### Default Parameters (ES06)
```js
// one default parameter
function items(item = "myDefaultItem") {
    console.log(`Item in List: ${item}`);
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
- `return` statement is skipped!

```js
// one parameter
const increase = input => input++; // be aware, increased value gets returned only!
const squareNum = num => num*num;  // no manipulation on the passed parameter/object

// zero or multiple parameters
const add = (a, b) => a + b;
const pi = () => 3.14;

```




