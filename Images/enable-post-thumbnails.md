## Enable post thumbnails
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Images/enable-post-thumbnails.md) 
```php
add_action('after_setup_theme', 'my_enable_thumbnails');
function my_enable_thumbnails() {
  add_theme_support('post-thumbnails');
}
```