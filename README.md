# sassy-colors
SCSS that auto-generates named color classes and applies corresponding background colors.

Given a color list like so...

```scss
$colors: (
  black: #000000,
  white: #FFFFFF,
  red:   #CC0000,
);
```

...you can get CSS like this...

```css
.tile.black {
  background: #000000;
}
.tile.black:hover {
  background: #404040;
}
.tile.white {
  background: #FFFFFF;
}
.tile.white:hover {
  background: white; /* [1] */
}
.tile.red {
  background: #CC0000;
}
.tile.red:hover {
  background: #ff4d4d;
}
```

**NOTE:** [1] SCSS spits out the CSS color name `white` via the `lighten()` function. It wasn't me, I swear!
