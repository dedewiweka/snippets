## Remove admin bar
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Tweaks/remove-admin-bar.md) 
```php
add_action('after_setup_theme', 'my_remove_admin_bar');
function my_remove_admin_bar() {
  if(!(current_user_can('administrator') && is_admin())) {
    show_admin_bar(false);
  }
}
```