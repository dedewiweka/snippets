## Change permalink base
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Permalinks/change_permalinks_base.md) 
```php
add_action('init', 'my_change_permalink_base');
function my_change_permalink_base() {
  global $wp_rewrite;

  $wp_rewrite->pagination_base = 'page';
  $wp_rewrite->search_base = 'search';
  $wp_rewrite->author_base = 'author';
}
```