# [Scroll Bars](https://alligator.io/css/css-scrollbars/)

```scss
/* The emerging W3C standard
   that is currently Firefox-only */
* {
    scrollbar-width: thin;
    scrollbar-color: blue orange;
}

/* Works on Chrome/Edge/Safari */
*::-webkit-scrollbar {
    width: 12px;
}

*::-webkit-scrollbar-track {
    background: orange;
}

*::-webkit-scrollbar-thumb {
    background-color: blue;
    border-radius: 20px;
    border: 3px solid orange;
}
```
