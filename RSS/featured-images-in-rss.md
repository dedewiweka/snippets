## Featured images in RSS

### Code Snippet

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
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).
