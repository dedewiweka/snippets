## Exclude category from archieve

### Code Snippet

```php
add_action('pre_get_posts', 'my_exclude_category_from_archive');
function my_exclude_category_from_archive($query) {
  // Exclude from the main archive, but display on the category archive
  // Must add is_admin() so posts are displayed in WP Administration Posts -> All posts
  if($query->is_main_query() && !is_admin() && $query->query['category_name'] !== 'custom-category-slug') {
    // Put category ID in the array
    $query->set('category__not_in', array(10));
  }
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).