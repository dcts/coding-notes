# !important

- There is one thing that is even more specific than IDs: `!important`. It can be applied to specific attributes instead of full rules. It will override any style no matter how specific it is. As a result, it should almost never be used. Once `!important` is used, it is very hard to override.
- If you ever see `!important` used (or are ever tempted to use it yourself) we strongly recommend reorganizing your CSS.

```html
<!-- HTML -->
<p id="green">not green!</p>
```
```css
/* CSS */ 
#green {color: green;}
p {color: blue !important}

/* !important overrides even the id-selector!*/
```