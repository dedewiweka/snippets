## GET category image
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/get-category-image.md) 
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