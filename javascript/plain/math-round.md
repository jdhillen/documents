[Math - Round](https://jimfrenette.com/javascript/helper-functions/)
===

```javascript
/**
 * round to decimal place
 *
 * @param num number to round
 * @param dec number of decimal places to round to
 */

function _round(num, dec) {
    return Math.round(num * Math.pow(10, dec)) / Math.pow(10, dec);
}
```
