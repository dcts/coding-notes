# Factory Functions

- function that creates instances of objects!
- comparison classes vs factory functions (ff)
  - classes use **`constructor()`** function and **`new`** keyword for instantiation.
  - classes use **`this`** keyword to reference fields, while ff have local scope of all variables defined insied them.
  - classes can inherit from other classes (more complex structures possible)
  - factoryFunctions are encapsuled -> you can define what you export with `Object.freeze({method1, method2})` (not sure how that works). See this [blogpost](https://medium.freecodecamp.org/class-vs-factory-function-exploring-the-way-forward-73258b6a8d15)


### Factory Function (with Function Expression)
```js
const createAnimal = (name, age, sound) => {
  return {
    name: name,
    age: age,
    makeSound () {
      console.log(sound);
    }
  }
}

const cat = createAnimal('whiskers', 2, 'miau');
cat.makeSound();

const dog = createAnimal('Honigkuchen', 5, 'wuff');
dog.makeSound();
```

### Factory Function (with Function Declaration)

```js
function createAnimal(name, age, sound){
    var name = name;
    var age = age;
    function makeSound(){
        console.log(sound); 
    }
    return Object.freeze({  // export object
        makeSound           // only export function makeSoun, no fields!
    });
}
```

### Property Value Shorthand in Factory Functions
```js
const createAnimal = (name, age) => {
  return {
    name,
    age
  }
}
```