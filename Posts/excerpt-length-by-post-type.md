## Excerpt length by post ID
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Posts/excerpt-length-by-post-type.md) 
```php
add_filter('excerpt_length', 'my_excerpt_length');
function my_excerpt_length($length) {
  global $post;

  if($post->post_type == 'post') {
    return 40;
  } else {
    return 60;
  }
}
```