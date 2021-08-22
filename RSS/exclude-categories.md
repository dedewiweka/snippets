## Exclude Categories
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/RSS/exclude-categories.md) 
```php
add_filter('pre_get_posts', 'my_exclude_category');
function my_exclude_category($query) {
  if($query->is_feed()) {
    $query->set('cat', '-5, -2, -3');
  }

  return $query;
}
```