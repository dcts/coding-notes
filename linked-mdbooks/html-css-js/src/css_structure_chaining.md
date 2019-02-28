# Chaining Selectors

We have 3 types of selectors `name`, `class` and `id`. We can combine these 3 different types by chaining them. We have to respect some rules:

- if you include a nameselector, start with the name-selector
- you can't chain multiple name-selectors
- chain as much class-selectors as you want by adding `.classname`
- you can chain also **one** id-selector by adding `#idname`
- no spaces


## Combinations of Names, Classes, IDs

### 1. multiple classes
selects all html elements with class `red`
```css
/* multiple classes (no id, no name) */
.red.bold { ... }

/* multiple classes and id (no name) */
.red.bold#id1 { ... }

/* name (h1) and id */
h1#id1 { ... }

/* name (h1) and class */
h1.class1 { ... }

/* name (h1) and multiple classes*/
h1.class1.class2.class3 { ... }

/* name (h1) with multiple classes and id */
/* ordering doesnt matter */
h1.red.bold#id1 { ... }
h1.bold#id1.red { ... }   
```

