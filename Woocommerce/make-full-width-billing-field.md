## Woocommerce Make Full Width Billing Field
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/make-full-width-billing-field.md) 
```php
//MAKE BILLING FIELD WIDTH 100%
function custom_billing_css_styles() {
    ?>
<style>
.woocommerce .col2-set .col-1, .woocommerce-page .col2-set .col-1 {float: none !important;width: 100% !important;}

</style>
    <?php
};
add_action( 'woocommerce_checkout_before_customer_details', 'custom_billing_css_styles' );
```