# [Leading Zeros](https://stackoverflow.com/questions/2998784/how-to-output-numbers-with-leading-zeros-in-javascript)

```javascript
/**
 * round to decimal place
 *
 * @param num number to pad
 * @param size number of leading zeros
 */

function leadingZeros(num, size) {
    let num = num.toString();
    while (num.length < size) num = "0" + num;
    return num;
}
```
