## Post thumbnails
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Setup/post-thumbnails.md) 
```php
add_action('after_setup_theme', 'my_theme_setup');
function my_theme_setup() {
  add_theme_support('post-thumbnails');
}
```