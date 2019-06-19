[Get Type](https://ultimatecourses.com/course/javascript-basics/correctly-type-checking-objects)
===

Get the type of a variable in the most reliable way in Javascript

```javascript
function getType(obj) {
  return Object.prototype.toString
    .call(obj)
    .slice(8, -1)
    .toLowerCase();
}
```