## Meta query
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/WP%20Query/meta-query.md) 
```php
$args = array(
  'post_type'       => 'your_post_type',
  'posts_per_page'  => -1,
  'meta_key'        => 'field_key',
  'meta_query'      => array(
    array(
      'key'         => 'field_key',
      'value'       => 'your_value',
      'compare'     => 'comparison_operator'
    )
    ),
    'orderby'       => 'meta_value',
    'order'         => 'ASC'
);

$query = new WP_Query($args);

// The loop ...
```