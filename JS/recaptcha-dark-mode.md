## Recaptcha dark mode
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/JS/recaptcha-dark-mode.md) 
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