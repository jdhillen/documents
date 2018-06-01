[Remove Styles](http://form.guide/best-practices/validate-email-address-using-javascript.html)
===

Remove all stlyes from an html string

```javascript
function removeStyles(a) {
    return a.replace(/style="[^"]*"/g, "");
}
```