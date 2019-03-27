# Function Expression / Anonymous Function

- anonymous functions -> have no function identifier (no name)
- can be stored in variables!
- use case: to pass functions into other functions we can use function expressions
```js
const x = function (a, b) {
	return a * b
};
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
