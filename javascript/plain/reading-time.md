# [Reading Time](https://dev.to/michaelburrows/calculate-the-estimated-reading-time-of-an-article-using-javascript-2k9l)

```html
<article id="article">
  <h1>Lorem ipsum dolor sit amet</h1>
  <p>
    Minus ullam est commodi facere repudiandae sit. Ab quibusdam totam veniam ducimus ut consequatur sit. Ea et nulla quaerat. Et temporibus
    quas numquam quas dolor vero accusantium numquam.
  </p>
  <!-- repeat <p> tag several times here -->
</article>
```

```javascript
function calcReadingTime(id) {
  const text = document.getElementById(id).innerText;
  const wpm = 250;
  const words = text.trim().split(/\s+/).length;
  const time = Math.ceil(words / wpm);
  return time;
}

calcReadingTime('article');
```
