## Change login errors
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Security/change-login-errors.md) 
```php
add_filter('login_errors', 'no_login_errors');
function no_login_errors() {
    return 'Something went wrong. Please try again!';
}
```
