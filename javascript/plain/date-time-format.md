# [DateTimeFormat](https://twitter.com/wesbos/status/1185263826029174784?s=20)

```javascript
const now = new Date();

new Intl.DateTimeFormat("en-US", { dataStyle: "full" }).format(now);
// Tuesday, October 15, 2020
new Intl.DateTimeFormat("en-US", { dataStyle: "long" }).format(now);
// October 15, 2020
new Intl.DateTimeFormat("en-US", { dataStyle: "medium" }).format(now);
//Oct 15, 2020
new Intl.DateTimeFormat("en-US", { dataStyle: "short" }).format(now);
// 10/15/20
new Intl.DateTimeFormat("fr-CA", { dataStyle: "long" }).format(now);
// 15 octobre 2020

// Alternative
const options = { weekday: "long", hour: "numeric" };
new Intl.DateTimeFormat("en-US", options).format(new Date());
// Friday, 2 PM
```
