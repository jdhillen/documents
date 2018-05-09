[Prevent Mobile Font Scaling](http://www.kaspertidemann.com/preventing-mobile-safari-from-upscaling-font-sizes/)
===

```scss
body, html {
    -webkit-text-size-adjust: none;
    -moz-text-size-adjust: none;
    -ms-text-size-adjust: none;
    -o-text-size-adjust: none;
}
```