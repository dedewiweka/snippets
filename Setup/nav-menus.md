## Navigation menus
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Setup/nav-menus.md) 
```php
add_action('after_setup_theme', 'my_theme_setup');
function my_theme_setup() {
  register_nav_menu('main', __('Main Menu', 'mytheme'));
}
```