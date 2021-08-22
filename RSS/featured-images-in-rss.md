## Featured images in RSS
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/RSS/featured-images-in-rss.md) 
```php
add_filter('the_excerpt_rss', 'my_rss_post_thumbnail');
add_filter('the_content_feed', 'my_rss_post_thumbnail');
function my_rss_post_thumbnail($content) {
  global $post;
  if(has_post_thumbnail($post->ID)) {
    $content = '<div>' . get_the_post_thumbnail($post->ID) . '</div>' . get_the_content();
  }

  return $content;
}
```