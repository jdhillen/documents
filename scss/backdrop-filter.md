# [Backdrop Filter](https://css-tricks.com/backdrop-filter-effect-with-css/)

```scss
.container {
    background: rgba(0, 0, 0, 0.8);
}

@supports (-webkit-backdrop-filter: none) or (backdrop-filter: none) {
    .container {
        -webkit-backdrop-filter: blur(10px);
        backdrop-filter: blur(10px);
    }
}
```
