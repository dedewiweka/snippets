## Woocommerce Custom Price Using URL Parameter

### License

You may use this codes and snippets under [GNU General Public License v3.0](https://github.com/dedewiweka/projects/blob/main/license)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).

### Code Snippet

```markdown
<? php;
//Use this code when needed

//Add Custom Price via URL Parameter
// get and set the custom product price in WC_Session
add_action( 'init', 'get_custom_product_price_set_to_session' );
function get_custom_product_price_set_to_session() {
    // Check that there is a 'custom_p' GET variable
    if( isset($_GET['add-to-cart']) && isset($_GET['cp']) 
    && $_GET['cp'] > 0 && $_GET['add-to-cart'] > 0 ) {
        // Enable customer WC_Session (needed on first add to cart)
        if ( ! WC()->session->has_session() ) {
            WC()->session->set_customer_session_cookie( true );
        }
        // Set the product_id and the custom price in WC_Session variable
        WC()->session->set('cp', [
            'id'    => (int) wc_clean($_GET['add-to-cart']),
            'price' => (float) wc_clean($_GET['cp']),
        ]);
    }
}

/* Change product price from WC_Session data
add_filter('woocommerce_product_get_price', 'custom_product_price', 900, 2 );
add_filter('woocommerce_product_get_regular_price', 'custom_product_price', 900, 2 );
add_filter('woocommerce_product_variation_get_price', 'custom_product_price', 900, 2 );
add_filter('woocommerce_product_variation_get_regular_price', 'custom_product_price', 900, 2 );
function custom_product_price( $price, $product ) {
    if ( ( $data = WC()->session->get('cp') ) && $product->get_id() == $data['id'] ) {
        $price = $data['price'];
    }
    return $price;
}

// Change cart item price from WC_Session data
add_action( 'woocommerce_before_calculate_totals', 'custom_cart_item_price', 20, 1 );
function custom_cart_item_price( $cart ){
    if ( is_admin() && ! defined( 'DOING_AJAX' ) )
        return;

    // Must be required since Woocommerce version 3.2 for cart items properties changes
    if ( did_action( 'woocommerce_before_calculate_totals' ) >= 2 )
        return;

    // Looo through our specific cart item keys
    foreach ( $cart->get_cart() as $cart_item ) {
        // Get custom product price for the current item
        if ( ( $data = WC()->session->get('cp') ) && $cart_item['data']->get_id() == $data['id'] ) {
            // Set the new product price
            $cart_item['data']->set_price( $data['price'] );
        }
    }
}
```
