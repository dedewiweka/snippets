## Exclude category from archieve
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Posts/exclude-category-from-archive.md) 
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