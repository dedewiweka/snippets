## Search only products

### Code Snippet

```php
add_action('pre_get_posts', 'my_search_products');
function my_search_products($query) {
	if(!is_admin() && is_search() && $query->is_main_query()) {
		$query->set('post_type', 'product');
	}
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).