## Unset ordering types
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/unset-ordering-types.md) 
```php
add_filter('woocommerce_catalog_orderby', 'my_unset_order_types');
function my_unset_order_types($options) {
	unset($options['popularity']);
	unset($options['rating']);

	return $options;
}
```