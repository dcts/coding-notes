# Comparison Operations

```js
// COMPARISON OPERATORS
/*  different datatypes are converted so the match!
 *  equality operator: == (datatype conversion is done)
 *  identity operator: === (datatypes must be the same) -> MORE STRICT!
 */
1=="1"               // true
"str"=="str"         // true
let num = 1;         // saved as number
num==="1"            // FALSE!!
num.toString()==="1" // true
true  === 1          // false
false === 0          // false
true   == 1          // true
false  == 0          // true

==       // equality operator
===      // identity operator
!=       // inequality operator
!==      // strictly inequality operator
>        // greater than (converts datatypes)
>=       // greater or equal than (converts datatypes)
<        // less than (converts datatypes)
<=       // less or equal than (converts datatypes)

// identity vs equality operator
"test" === ['test']  // false
"test" ==  ["test"]  // true (typeconversion done)
"3" === 3            // false
"3" ==  3            // true (typeconversion done)

&&       // inclusive AND
||       // inclusive OR
!        // not operator (reverses value of a boolean)
!true    // false 
```
