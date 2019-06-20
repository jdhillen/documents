[Button](https://codepen.io/hankchizljaw/pen/Vxpjvo)
===

```scss
$font-color: #FFFFFF;
$bg-color: #0069ED;
$bg-focus: #0053BA;

button {
    display: inline-block;
    border: none;
    padding: 1rem 2rem;
    margin: 0;
    text-decoration: none;
    background: $bg-color;
    color: $font-color;
    font-family: sans-serif;
    font-size: 1rem;
    cursor: pointer;
    text-align: center;
    transition: background 250ms ease-in-out, transform 150ms ease;
    -webkit-appearance: none;
    -moz-appearance: none;

    &:hover,
    &:focus {
        background: $bg-focus;
    }

    &:focus {
        outline: 1px solid $font-color;
        outline-offset: -4px;
    }

    &:active {
        transform: scale(0.99);
    }
}
```
