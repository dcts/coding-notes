# If Else

```js
if (true) {
	// do something
} else if (false /*another condition*/) {
	// do something
} else {
	// do something
}
```

### Ternary If-Else

- semicolon only at the end of the line
```js
(condition) ? (do if true) : (do if false);
age>=18     ? "adult"      : "child";        // returns "adult" or "child"!

// also works with function-calls inside
age>=18 ? console.log("over 18") : console.log("under 18");
```