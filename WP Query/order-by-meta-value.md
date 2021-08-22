## Order by meta value

### Code Snippet

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
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).