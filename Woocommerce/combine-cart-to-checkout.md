## Woocommerce Combine The Cart To Checkout Page

### Code Snippet

```markdown
// COMBINE THE CART TO CHECKOUT PAGES
	add_action( 'woocommerce_before_checkout_form', 'cart_on_checkout_page_only', 5 );
	function cart_on_checkout_page_only() {
		if ( is_wc_endpoint_url( 'order-received' ) ) return;
		echo do_shortcode('[woocommerce_cart]');
	}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).

