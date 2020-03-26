# [Mixin - Covering](https://css-tricks.com/snippets/sass/covering-mixin/)

```scss
@mixin coverer {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}

// - Example ---------------------------------------------------------------------------------------
.modal {
    @include coverer;
    background: rgba(black, 0.5);
    z-index: 1000;
}
```
