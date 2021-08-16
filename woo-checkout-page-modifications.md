## Woocommerce Checkout Page Modifications

### License

[GNU General Public License v3.0](https://github.com/dedewiweka/projects/blob/main/license)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).


### Code Snippet

```markdown
<? php;
//Use this code when needed

// COMBINE THE CART TO CHECKOUT PAGES
	add_action( 'woocommerce_before_checkout_form', 'cart_on_checkout_page_only', 5 );
	function cart_on_checkout_page_only() {
		if ( is_wc_endpoint_url( 'order-received' ) ) return;
		echo do_shortcode('[woocommerce_cart]');
	}

// HIDE HAVE COUPON MESSAGE FIELD
remove_action( 'woocommerce_before_checkout_form', 'woocommerce_checkout_coupon_form', 10 ); 

//HIDE ADDED TO CART MESSAGE FIELD
	add_filter( 'wc_add_to_cart_message', 'remove_add_to_cart_message' );
	function remove_add_to_cart_message() {
		return;
	}

//MAKE BILLING FIELD WIDTH 100%
function custom_billing_css_styles() {
    ?>
<style>
.woocommerce .col2-set .col-1, .woocommerce-page .col2-set .col-1 {float: none !important;width: 100% !important;}

</style>
    <?php
};
add_action( 'woocommerce_checkout_before_customer_details', 'custom_billing_css_styles' );

//MAKE SHIPPING FIELD WIDTH 100%
function custom_shipping_css_styles() {
    ?>
<style>.woocommerce .col2-set .col-2, .woocommerce-page .col2-set .col-2 {float: none !important;width: 100% !important;}</style>
    <?php
};
add_action( 'woocommerce_checkout_before_customer_details', 'custom_shipping_css_styles' );


```
