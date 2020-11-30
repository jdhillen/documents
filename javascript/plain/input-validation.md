[Validation](#)
===

#### [Email](http://form.guide/best-practices/validate-email-address-using-javascript.html)

```javascript
function validateEmail(a) {
    var regex = /^(([^<>()[\]\\.,;:\s@\"]+(\.[^<>()[\]\\.,;:\s@\"]+)*)|(\".+\"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
    return regex.test(a) ? true : false;
}
```

---

#### [Phone Number](https://www.w3resource.com/javascript/form/phone-no-validation.php)

```javascript
function validatePhone(a) {
    var regex = /^\(?([0-9]{3})\)?[-. ]?([0-9]{3})[-. ]?([0-9]{4})$/;
    return regex.test(a);
}
```
