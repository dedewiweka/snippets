## Remove first and last class
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/remove-first-and-last-class.md) 
```php
add_filter('post_class', 'my_prefix_post_class', 21);
function my_prefix_post_class($classes) {
	if('product' == get_post_type() && is_search()) {
		$classes = array_diff($classes, array('first', 'last'));
	}
	return $classes;
}
```