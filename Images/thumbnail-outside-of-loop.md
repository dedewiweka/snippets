## Thumbnail outside of loop
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Images/thumbnail-outside-of-loop.md) 
```php
global $post;
$image_arr = wp_get_attachment_image_src(get_post_thumbnail_id($post->ID), 'full');

if(!empty($image_arr)) {
  $image = $image_arr[0];
}
```