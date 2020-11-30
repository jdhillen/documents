# [Array Methods](https://dev.to/denicmarko/10-javascript-array-methods-to-simplify-your-code-56f)

filter()

```javascript
const words = ["HTML", "CSS", "JavaScript", "Python", "Java"];
const longWords = words.filter((word) => word.length > 4);
console.log(longWords);
```

forEach()

```javascript
const words = ["HTML", "CSS", "JavaScript", "Python", "Java"];
words.forEach((word) => console.log(word));
```

some()

```javascript
const myArray = [1, 2, 3, 4, 5];
const evenExists = myArray.some((element) => element % 2 === 0);
console.log(evenExists); // true
```

every()

```javascript
const myArray = [1, 2, 3, 4, 5];
const allEven = myArray.every((element) => element % 2 === 0);
console.log(allEven); // false
```

includes()

```javascript
const numbers = [1, 2, 3, 4, 5];
console.log(numbers.includes(2)); // true
console.log(numbers.includes(8)); // false
```

map()

```javascript
const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map((x) => x * 2);
console.log(doubled); // [2, 4, 6, 8, 10]
```

reduce()

```javascript
const numbers = [10, 20, 30, 40];
const sum = numbers.reduce((x, y) => x + y);
console.log(sum); // 100
```

sort()

```javascript
const techs = ["HTML", "CSS", "JavaScript"];
techs.sort();
console.log(techs); // ['CSS', 'HTML', 'JavaScript']

const numbers = [1, 30, 4, 21, 10000];
numbers.sort((x, y) => x - y);
console.log(numbers); // [1, 4, 21, 30, 10000]
```

find()

```javascript
const numbers = [7, 14, 8, 128, 56];
const found = numbers.find((element) => element > 10);
console.log(found); // 14
```

findIndex()

```javascript
const numbers = [5, 12, 8, 130, 44];
const indexFound = numbers.findIndex((element) => element > 15);
console.log(indexFound); // 3
```
