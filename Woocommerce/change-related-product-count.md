## Change related product count

### Code Snippet

```php
add_filter('woocommerce_output_related_products_args', 'my_related_product_count');
function my_related_product_count($args) {
	$args['posts_per_page'] = 3;
	$args['columns'] = 3;
	return $args;
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).