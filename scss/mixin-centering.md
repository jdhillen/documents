[Mixin - Centering](https://css-tricks.com/snippets/sass/centering-mixin/)
===

```scss
@mixin centerer($horizontal: true, $vertical: true) {
    position: absolute;
    @if ($horizontal and $vertical) {
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    } @else if ($horizontal) {
        left: 50%;
        transform: translate(-50%, 0);
    } @else if ($vertical) {
        top: 50%;
        transform: translate(0, -50%);
    }
}


// - Example ---------------------------------------------------------------------------------------
.element0 {
    @include centerer;
}

.element1 {
    @include centerer(true, false);
}

.element2 {
    @include centerer(false, true);
}
```