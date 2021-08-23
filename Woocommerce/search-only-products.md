## Search only products
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/search-only-products.md) 
```php
add_action('pre_get_posts', 'my_search_products');
function my_search_products($query) {
	if(!is_admin() && is_search() && $query->is_main_query()) {
		$query->set('post_type', 'product');
	}
}
```