## Recaptcha dark mode

### Code Snippet

```js
// Set reCaptcha to dark mode
document.addEventListener('DOMContentLoaded', function () {
  var footerForm = document.querySelectorAll('.parent-element div.g-recaptcha');
  var contactForm = document.querySelectorAll('.another-parent-element div.g-recaptcha');

  function setDarkTheme(el) {
    el.setAttribute('data-theme', 'dark');
  }

  footerForm.forEach(setDarkTheme);
  contactForm.forEach(setDarkTheme);
});
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).