## Get rpoduct featured image

### Code Snippet

```php
  //Inside the post loop
   $image = wp_get_attachment_image_src(get_post_thumbnail_id($loop->post->ID), 'single-post-thumbnail');
?>

  <img src="<?php echo $image[0]; ?>" alt="<?php the_title(); ">
 <?php 
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).