# CSS

**CSS** = **C**ascading **S**tyle **S**heet 

## Vocabulary & Syntax

<img src="pics/css-syntax.png" width="450px" />
- **CSS-Selector** — are used to "find" (or select) HTML elements based on their element name `tag`, id `#`, class `.`, attribute, and more. 
- **styling-rules** — are inside the curly brackets `{}`
- **style property** — for example `width`, `color` or `font-size`
- **property-value** — for example `100px`, `red` or `14px`. Value is surrounded by quotations marks `""`.

## Multiple CSS-Selectors

```css
/* seperated by comma 
 * can be classes, id's or tags, doesnt really matter */ 
h1, h2, p, 
.banners, .container,
#top-logo, #footer-logo {
  property: value;
  property: value;
  property: value;
}
```