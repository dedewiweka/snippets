## Logout redirect
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Users/logout-redirect.md) 
```php
add_action('wp_logout', 'my_redirect_after_logout');
function my_redirect_after_logout() {
  wp_redirect(esc_url(home_url('/')));
  exit;
}
```