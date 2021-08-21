## Excerpt length by post ID

### Code Snippet

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
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).