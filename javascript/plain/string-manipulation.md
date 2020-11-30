[String Manipulation](#)
===

## Remove Stlyes from an HTML string

```javascript
function removeStyles(a) {
    return a.replace(/style="[^"]*"/g, "");
}
```

---

## Strip HTML all tags from an HTML string

```javascript
function removeHtmlTags(a) {
    return a.replace(/(<([^>]+)>)/ig,"");
}
```

---

## Split a paragraph into a sentence object

```javascript
function sentenceSplit(a) {
    var regex = /[^\.!\?]+[\.!\?]+/g;
    return a.match(regex);
}
```
