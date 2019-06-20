[Function - Black and White Opacity](https://css-tricks.com/snippets/sass/black-white-opacity-mixins/)
===

```scss
@function black($opacity) {
    @return rgba(black, $opacity);
}

@function white($opacity) {
    @return rgba(white, $opacity);
}


// - Example ---------------------------------------------------------------------------------------
.element0 {
    color: black(0.5);
}

.element1 {
    color: white(0.5);
}
```
