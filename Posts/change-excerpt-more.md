## Change excerpt more
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Posts/change-excerpt-more.md) 
```php
//Remove [...] from excerpt
add_filter('excerpt_more', 'my_excerpt_more');
function my_excerpt_more($more) {
    return '';
}
```