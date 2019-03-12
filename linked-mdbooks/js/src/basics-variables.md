# Variables

```js
// declaring variables
// variable names can also contain $ and _
var varName;                    // function scope, heusted!
let varName;                    // ES06 Standard, blockscope
const varName = "initialValue"; // variables which cannot be reassigned,
                                // must be initialized during declaration
```

```js
// VARIABLE SCOPE:
/*  1 functionscope VS blockscope!
 *    ..if declared in function it is not availible outside of it
 *    ..if declared in block (loops for example)
 *    var is availible outside of the block/loop
 *    let is NOT availible outside of the block/loop
 *  2 local vs global scope!
 *    ...it is possible to have the same variable name as global and local scope,
 *    in this case the local scope is precedenced over the global!!
 */
```

### short circuit assignments
- assigns `myVariable` the value of `myName` in case `myName` is truthly and `"no-name-selected!"` in case of falsly. 
- In the below example the empty string will be evaluated falsly and the string `"no-name-selected!"` will be assigned!
```js
let myName = "";
let myVariable = myName || "no-name-selected!";
```