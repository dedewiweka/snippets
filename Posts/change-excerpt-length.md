## Change excerpt length
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Posts/change-excerpt-length.md) 
```php
add_filter('excerpt_length', 'my_excerpt_length');
function my_excerpt_length($length) {
    return 40;
}
```