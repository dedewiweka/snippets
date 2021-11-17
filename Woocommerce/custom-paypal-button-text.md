/**
 * Custom PayPal button text
 *
 */

add_filter( 'gettext', 'ld_custom_paypal_button_text', 20, 3 );
function ld_custom_paypal_button_text( $translated_text, $text, $domain ) {
	switch ( $translated_text ) {
		case 'Proceed to PayPal' :
			$translated_text = __( 'Your new Paypal button text here', 'woocommerce' );
			break;
	}
	return $translated_text;
}
