# [Mixin - Font Smoothing](https://medium.com/@MateMarschalko/improving-font-rendering-with-css-3383fc358cbc)

```scss
.smooth {
    -webkit-text-stroke: 0.35px;
    -webkit-font-smoothing: antialiased;
    text-rendering: optimizeLegibility;
}

// - Example ---------------------------------------------------------------------------------------
html,
body {
    @extend .smooth;
}
```
