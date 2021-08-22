## Unset ordering types

### Code Snippet

```php
add_filter('woocommerce_catalog_orderby', 'my_unset_order_types');
function my_unset_order_types($options) {
	unset($options['popularity']);
	unset($options['rating']);

	return $options;
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).