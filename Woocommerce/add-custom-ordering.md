## Add custom ordering
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/add-custom-ordering.md) 
```php
//Make ordering arguments
add_filter('woocommerce_get_catalog_ordering_args', 'my_custom_ordering_args');
function my_custom_ordering_args($args) {
	$orderby_value = isset($_GET['orderby']) ? woocommerce_clean($_GET['orderby']) : apply_filters('woocommerce_default_catalog_orderby', get_option('woocommerce_default_catalog_orderby'));

	if('alphabetical-desc' == $orderby_value) {
		$args['orderby'] = 'title';
		$args['order'] = 'desc';
	}

	if('alphabetical-asc' == $orderby_value) {
		$args['orderby'] = 'title';
		$args['order'] = 'asc';
	}

	return $args;
}
```
```php
// Set ordering types
add_filter('woocommerce_default_catalog_orderby_options', 'my_custom_ordering_orderby');
add_filter('woocommerce_catalog_orderby', 'my_custom_ordering_orderby');
function my_custom_ordering_orderby($sortby) {
	$sortby['alphabetical-asc'] = __('Order by name (A - Z)', 'text-domain');
	$sortby['alphabetical-desc'] = __('Order by name (Z - A)', 'text-domain');

	return $sortby;
}
```