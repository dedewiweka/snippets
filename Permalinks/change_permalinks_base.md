## Change permalink base

### Code Snippet

```php
add_action('init', 'my_change_permalink_base');
function my_change_permalink_base() {
  global $wp_rewrite;

  $wp_rewrite->pagination_base = 'page';
  $wp_rewrite->search_base = 'search';
  $wp_rewrite->author_base = 'author';
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).