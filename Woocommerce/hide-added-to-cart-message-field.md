## Woocommerce Hide Added To Cart Message Field
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/hide-added-to-cart-message-field.md) 
```php
//HIDE ADDED TO CART MESSAGE FIELD
	add_filter( 'wc_add_to_cart_message', 'remove_add_to_cart_message' );
	function remove_add_to_cart_message() {
		return;
	}
```