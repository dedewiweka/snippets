## Exclude Categories

### Code Snippet

```php
add_filter('pre_get_posts', 'my_exclude_category');
function my_exclude_category($query) {
  if($query->is_feed()) {
    $query->set('cat', '-5, -2, -3');
  }

  return $query;
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).
