# Arrow Function

```js
const x = (a, b) => {
	return a * b
};
console.log(x(2,3));  // 6
```

**concise body arrow functions**
- functions that take only one parameter don't need to be enclosed in parentheses!
- zero or multiple parameters have to be enclosed in parentheses
- single line blocks do not neet curly braces `{}`!
- `return` statement is skipped!
- do NOT use arrowfunctions in classes, since `this.`

```js
// one parameter
const increase = input => input++; // be aware, increased value gets returned only!
const squareNum = num => num*num;  // no manipulation on the passed parameter/object

// zero or multiple parameters
const add = (a, b) => a + b;
const pi = () => 3.14;

```




