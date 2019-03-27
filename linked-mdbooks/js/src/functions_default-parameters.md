# Default Parameters

### Default Parameters (since ES06)
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
