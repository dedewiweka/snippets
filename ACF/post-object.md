## Post object
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/post-object.md) 
```php
$post_obj = get_field('my_post_obj');
if(!empty($post_obj)) {
  global $post;
  $post = $post_obj;
  setup_postdata($post);
  /**
   * Insert markup
   */
  wp_reset_postdata();
}
```