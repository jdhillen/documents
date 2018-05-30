[Map](#)
===

From [Chris Riebschlager](https://gitlab.com/riebschlager)

```javascript
function map(input, oldMin, oldMax, newMin, newMax) {
    return ((input - oldMin) / (oldMax - oldMin)) * (newMax - newMin) + newMin;
}
```