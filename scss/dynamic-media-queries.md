# [Dynamic Media Queries](https://stackoverflow.com/questions/36957904/media-queries-in-sass)

```scss
$size__site_content_width: 1024px;

/* Media Queries */ Not necessarily correct, edit these at will 
$media_queries : (
    'mobile'    : "only screen and (max-width: 667px)",
    'tablet'    : "only screen and (min-width: 668px) and (max-width: $size__site_content_width)",
    'desktop'   : "only screen and (min-width: ($size__site_content_width + 1))",
    'retina2'   : "only screen and (-webkit-min-device-pixel-ratio: 2) and (min-resolution: 192dpi)",
    'retina3'   : "only screen and (-webkit-min-device-pixel-ratio: 3) and (min-resolution: 288dpi)",
    'landscape' : "screen and (orientation:landscape) ",    
    'portrait'  : "screen and (orientation:portrait) "
);

@mixin breakpoint($breakpoints) {
  $conditions : ();
  @each $breakpoint in $breakpoints {
    // If the key exists in the map
    $conditions: append(
      $conditions,
      #{inspect(map-get($media_queries, $breakpoint))},
      comma
    );
  }

  @media #{$conditions} {
    @content;
  }
}
```

```scss
#masthead {
  background: white;
  border-bottom:1px solid #eee;
  height: 90px;
  padding: 0 20px;
  @include breakpoint(mobile desktop) {
    height:70px;
    position:fixed;
    width:100%;
    top:0;
  }
}
```
