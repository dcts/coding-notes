# Structure and Specificity


**cascading** order = the most specific css-selector is applied! Less specific selectors will be overriden.
1. **tagname**: least specific
2. **class**: more specific, recurrent styling
3. **id**: most specific. One element per id only, applying the same id to multiple elements is invalid HTML and should be avoided

```css
/* tag-level */
body { }

/* class-level */
#myClass { }

/* id-level */
.myId { }
```

