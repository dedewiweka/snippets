## Addproduct tab
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/add-product-tabs.md) 
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