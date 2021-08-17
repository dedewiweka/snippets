## Woocommerce Combine The Cart To Checkout Page

### License

[GNU General Public License v3.0](https://github.com/dedewiweka/projects/blob/main/license)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).


### Code Snippet

```markdown
// COMBINE THE CART TO CHECKOUT PAGES
	add_action( 'woocommerce_before_checkout_form', 'cart_on_checkout_page_only', 5 );
	function cart_on_checkout_page_only() {
		if ( is_wc_endpoint_url( 'order-received' ) ) return;
		echo do_shortcode('[woocommerce_cart]');
	}

```
