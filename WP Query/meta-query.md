## Meta query

### Code Snippet

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
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).