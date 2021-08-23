## Get rpoduct featured image
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/get-product-featured-image.md) 
```php
  //Inside the post loop
   $image = wp_get_attachment_image_src(get_post_thumbnail_id($loop->post->ID), 'single-post-thumbnail');
?>

  <img src="<?php echo $image[0]; ?>" alt="<?php the_title(); ">
 <?php 
```