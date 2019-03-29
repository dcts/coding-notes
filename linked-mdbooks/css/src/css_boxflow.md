# CSS Box Model

<img src="pics/css-box-model.png">

- margin (Platz ausserhalb vom Rand)
- border (Rand)
- padding (Platz zwischen Rand und Inhalt)
- content (Inhalt)

# Example

```css
div {
	padding: 10px;
	border: 2px;
	margin: 10px;
}
```

### Border

```css
/* thickness, style and color in 1 statement! */
border: px style color;
border: 12px solid red; /* dotted, dashed, double, none */

/* make borders round */
boder-radius: 10px
boder-radius: 100% (=circle)
```

### Padding

```css
/* PADDING */ 
padding: 10px; /* = on all sides 10px!*/

/* same as...*/
pading-top: 10px;
pading-right: 10px;
pading-bottom: 10px;
pading-left: 10px;

/* padding: v1 v2 v3 v4; -> top / right / bottom / left 
 * padding: v1 v2 v3;    -> top / right+left / bottom
 * padding: v1 v2;       -> top+bottom / right+left
 */
```

### Margin

```css
/* - same as padding concerning syntax
 * - space between border and other elements!
 * - margins add up horizontally!
 * - margins collapse vertical (higher is applied)
 */

maring: 0 auto

/* MIN / MAX SIZE */
min-width: 200px;
max-width: 400px;
min-height: 200px;
max-height: 400px;
```
