# RGB(a)

- **R**ed, **G**reen, **B**lue.
- `color: rgb(R, G, B)`
- **red**: `rgb(255, 0, 0)`
- **green**: `rgb(0, 255, 0)`
- **blue**: `rgb(0, 0, 255)`

### Grey Scale (Black / White)

when all values for `R`, `G` and `B` are the same, we move across a greyscale where `0` is black and `255` is white!
```css
/* black */ 
rgb(0,0,0)

/* dark grey */ 
rgb(20,20,20)

/* light grey */ 
rgb(220,220,220)

/* white */ 
rgb(255,255,255)
```

### Alpha-Channel (Opacity)

- Syntax: `color: rgba(R,G,B,a)`
- transparent when `a=0` 
- no opacity when `a=1` (default when using rgb)
