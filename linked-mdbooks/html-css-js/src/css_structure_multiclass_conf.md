# Conflicts (multiple class)

- Ordering of class-selectors does matter inside the CSS-file
- CSS-file: when two css-selectors have the same specificity (e.g. they are both classes) and conflicting styles, then the style of the selector is applied that is written at the end of the file (the latest instruction is applied)
- Ordering of the class-attribute-values (inside the HTML-file) does **not** matter
- if the ordering switches inside the CSS-file

```html
<!-- HTML -->
<p class="red green">
  wil be displayed red, not green! (.red is later defined than .green)
</p>
```

```css
/* CSS */ 
.green {
  text-transform: uppercase;
}
.red {
  text-transform: capitalize;
}
```

- a chained class-selector is more specific than an pure class selector, but less specific than a id-selector!
```html
<!-- HTML -->
<p id="my-name" class="red">Hans Müller</p>
```
```css
/* CSS */
.red {color: red;}
p.red {color: darkred;}
#my-name {color: hotpink;}

/* text will be displayed hotpink
 * ordering in the css file does not impact the outcome,
 * since none of the css-selectors has the same specificty! 
 * -> id > chained class > class */ 
```