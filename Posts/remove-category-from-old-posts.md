## Exclude category from old posts

### Code Snippet

```php
// Execute this hook with a cron job
add_action('my_remove_cats', 'my_remove_cats_exec');
function my_remove_cats_exec() {
  $posts = get_posts([
    'numberposts'     => -1,
    'category_name'   => 'slug-of-cat-to-remove',
    'date_query'      => [
      'after'         => date("Y-m-d H:i:s", strtotime('-180 days', current_time('timestamp'))),
    ]
  ]);

  if(!empty($posts)) {
    foreach($posts as $post) {
      wp_remove_object_terms($post->ID, 'slug-of-cat-to-remove', 'category');
    }
  }
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).