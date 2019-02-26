# Chaining Selectors

```html
<!-- HTML -->
<h1 class="red">will be red and bold</h1>
<p class="red">will be red only</p>
```

```css
/* CSS */ 
.red {
  color: red;
}
h1.red {
  font-style: bold;
}
```
- applies `color:red;` to all classes (for both `h1` and `p`)
- for `h1` there is additional a font-style defined (bold)
- this example is only demonstration, not best practice!