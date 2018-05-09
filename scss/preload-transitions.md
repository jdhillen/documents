[Transitions Only After Page Load](https://css-tricks.com/transitions-only-after-page-load/)
===

```scss
.preload * {
    -webkit-transition: none !important;
    -moz-transition: none !important;
    -ms-transition: none !important;
    -o-transition: none !important;
    transition: none !important;
}
```

```html
<body class="preload">

<script>
    // Then remove the class on page load
    $(window).load(function() {
        $("body").removeClass("preload");
    });
</script>
```