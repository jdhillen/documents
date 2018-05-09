[Function - Tint and Shade](https://css-tricks.com/snippets/sass/tint-shade-functions/)
===

```scss
/// Slightly lighten a color
/// @access public
/// @param {Color} $color - color to tint
/// @param {Number} $percentage - percentage of `$color` in returned color
/// @return {Color}
@function tint($color, $percentage) {
    @return mix(white, $color, $percentage);
}

/// Slightly darken a color
/// @access public
/// @param {Color} $color - color to shade
/// @param {Number} $percentage - percentage of `$color` in returned color
/// @return {Color}
@function shade($color, $percentage) {
    @return mix(black, $color, $percentage);
}


// - Example ---------------------------------------------------------------------------------------
.element0 {
    color: tint(#BADA55, 42%);
}

.element1 {
    color: shade(#663399, 42%);
}
```