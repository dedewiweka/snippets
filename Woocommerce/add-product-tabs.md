## Addproduct tab

### Code Snippet

```php
// Add extra tab to Woocommerce
add_filter('woocommerce_product_tabs', 'my_custom_tabs');
function my_custom_tabs($tabs) {
	$tabs['my_custom_tab'] = array(
		'title'     => __('My Custom Tab', 'Woocommerce'),
		'priority'  => 110,
		'callback'  => 'my_custom_tab_callback'
	);

	return $tabs;
}

function my_custom_tab_callback() {
  echo '<h2>' . __('My Custom Tab', 'Woocommerce') . '</h2>';
  // Echo your custom field here
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).