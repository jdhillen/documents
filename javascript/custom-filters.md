[Custom Filters](https://dev.to/machy44/lets-create-our-own-filter-method-in-js--5gh4)
===

```javascript
Array.prototype.customFilter = function(fun) {
    var filtered = [];
    for (let i = 0; i < this.length; i++) {
        if (fun(this[i], i, this)) filtered.push(this[i]);
    }
    return filtered;
};

var testArray = [1, 2, 3, 4, 5, 6];

var returnedArr = testArray.customFilter(function(element, index, arr) {
    return element > 5;
});

console.log(returnedArr);
```