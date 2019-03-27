# Linking CSS and HTML

### Linking via CSS-File

```html
<!-- add link in HEAD -->
<head>
  <link rel="stylesheet" type="text/css" src="css/style.css">
</head>
```

### Linking with `style` tag

```html
<!-- add style in HEAD -->
<head>
  <style>
    body {
      /* CSS styling for body here */ 
    }
    p {
      /* CSS styling for paragraph */
    }
  </style>
  <link rel="stylesheet" src="css/style.css">
</head>
```

### Inline-Linking

```html
<!--  -->
<p style="color: white; background-color: black;">
  white text on black background
</p>
```