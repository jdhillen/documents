# [Function - Tint and Shade](https://css-tricks.com/snippets/sass/tint-shade-functions/)

```scss
@function tint($color, $percentage) {
    @return mix(white, $color, $percentage);
}

@function shade($color, $percentage) {
    @return mix(black, $color, $percentage);
}

// - Example ---------------------------------------------------------------------------------------
.element0 {
    color: tint(#bada55, 42%);
}

.element1 {
    color: shade(#663399, 42%);
}
```
