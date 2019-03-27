# Switch

### break / default
- do not forget to `break` after each statement, otherwise the cases that follow will also be run! (If you omit the break statement, the next case will be executed even if the evaluation does not match the case.)
- It is not necessary to break the last case in a switch block. The block breaks (ends) there anyway
- The `default` case does not have to be the last case in the block (but if so don't forget to end the default case with a break!)

### matching and choosing cases
- Switch cases use strict comparison `(===)`
- The values must be of the same type to match.
- If multiple cases matches a case value, the first case is selected.
- If no matching cases are found, the program continues to the default label.

### Example
```js
switch (variable_type) {	
  case "string":
    // do something
    break;
  case "number":
    // do something
    break;
  case "undefined":
    // do something
    break;
  case "object"
    // do something
    break;
  default
    // do default
    break;          // "break" not mandatory
}
```

