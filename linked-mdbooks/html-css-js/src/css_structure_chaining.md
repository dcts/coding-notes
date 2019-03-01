# Chaining Selectors

We have 3 types of selectors `name`, `class` and `id`. We can combine these 3 different types by chaining them. We have to respect some rules:
- chaining always works with the `.` or `#` operator. 
- no spaces! Spaces are used for [nesting](css_structure_nesting.md), which is a different concept!
- if you include a name-selector, start with the name-selector
- you can't chain multiple name-selectors (one element cant be part of two tags)
- if you want to use two tagnames, you probably want to use [nesting](css_structure_nesting.md)
- chain as much class-selectors as you want by adding `.classname`
- you can chain also **one** id-selector by adding `#idname`

## Combinations of Names, Classes, IDs

```css
/* name */
h1 { ... }

/* name & class */
h1.class1 { ... }

/* classes */
.red.bold { ... }

/* classes & id */
.red.bold#id1 { ... }

/* name & classes */
h1.class1.class2.class3 { ... }

/* name & id */
h1#id1 { ... }

/* name & classes & id */
/* ordering doesnt matter */
h1.red.bold#id1 { ... }
h1.bold#id1.red { ... }   
```

