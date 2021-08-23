## Order by meta value
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/WP%20Query/order-by-meta-value.md) 
```php
$args = array(
  'post_type'       => 'your_post_type',
  'posts_per_page'  => -1,
  'meta_key'        => 'acf_field_name',
  'orderby'         => 'meta_value',
  'order'           => 'asc'
);

$query = new WP_Query($args);
```