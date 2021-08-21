## GET category image

### Code Snippet

```php
  $args = array(
    'taxonomy'    =>  'product_cat',
    'hide_empty'  =>  false,
  );
  $cats = get_terms($args);

  foreach($cats as $cat) : 
    $thumb_id = get_woocommerce_term_meta($cat->term_id, 'thumbnail_id', true);
    $thumb_img = wp_get_attachment_url($thumb_id);
?>
    <img src="<?php echo $thumb_img; ?>" alt="<?php echo $cat->name; ">
<?php 
  endforeach;
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).
