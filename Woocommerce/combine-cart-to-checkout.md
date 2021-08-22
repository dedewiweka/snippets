## Combine The Cart To Checkout Page
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/combine-cart-to-checkout.md) 
```php
// COMBINE THE CART TO CHECKOUT PAGES
	add_action( 'woocommerce_before_checkout_form', 'cart_on_checkout_page_only', 5 );
	function cart_on_checkout_page_only() {
		if ( is_wc_endpoint_url( 'order-received' ) ) return;
		echo do_shortcode('[woocommerce_cart]');
	}
```