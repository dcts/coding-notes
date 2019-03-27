# Destructed Assignments

```js
const animal = {
    type: "cat",
    name: "whiskas",
    preferences: {
        food: "mouses",
        activity: "sleep"
    }
};
// assign to new constant variable "type" and "name"
const { type } = animal;
const { name } = animal;
// you can also assign nested objects
// and also multiple destructured assignments!
const { food, activity } = animal.preferences;

console.log(type);     // "cat"
console.log(name);     // "whiskas"
console.log(food);     // "mouses"
console.log(activity); // "sleep"
```