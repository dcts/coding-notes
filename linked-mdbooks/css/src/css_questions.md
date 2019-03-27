# OPEN QUESTIONS

- best practice in CSS? Is it right that styles like "red" and "bold" should **NOT** be defined as classes, since then we "style" the content already inside the html code. If we want to redesign (choose other colors) then we have to rename our classnames in the HTML (thus chaning the HTML code), since we dont want a classname "green" having another color. Thats is painfull, am I right? Any pro tips / experiences with this? 
```html
<!-- VERSION 1 -->
<h1 class="red bold">my heading</h1>
.red {color: red;}
.bold {font-weight: bold;}

<!-- VERSION 2 -->
<h1 class="style1">my heading</h1>
.style1 {color:red; font-weight:bold;}

<!-- VERSION 3 -->
<h1 class="style1">my heading</h1>
h1.style1 {color:red; font-weight:bold;}

```

- Nested Elements: whats the use-case for this? I cant imagine any scenario where this is needed or cannot be acomplished with better classnames? I think its more clear to write more specific classnames than using this solution:
```css
/* why doing this? */
.main-container h1 { property-value }

/* instead of this */
.main-container-h1 {property-value }

/* obviously you have to write it down all the time, that sucks
 * but for styling its much clearer? Aaah or maybe not, idk lol!
```