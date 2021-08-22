## Change number of products per row
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/change-number-of-products-per-row.md) 
```php
add_filter('loop_shop_columns', 'my_loop_columns');
if(!function_exists('my_loop_columns')) {
	function my_loop_columns() {
		return 3;
	}
}
```