## Change related product count
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/change-related-product-count.md) 
```php
add_filter('woocommerce_output_related_products_args', 'my_related_product_count');
function my_related_product_count($args) {
	$args['posts_per_page'] = 3;
	$args['columns'] = 3;
	return $args;
}
```