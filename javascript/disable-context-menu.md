# [Disable Context Menu](https://www.codeinwp.com/snippets/disable-right-click-context-menu/)

```javascript
window.addEventListener(
    "contextmenu",
    function (e) {
        e.preventDefault();
    },
    false
);
```
