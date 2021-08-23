## Woocommerce Make Full Width Shipping Field
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/make-full-width-shipping-field.md) 
```php
//MAKE FULL WIDTH SHIPPING FIELD
function custom_shipping_css_styles() {
    ?>
<style>.woocommerce .col2-set .col-2, .woocommerce-page .col2-set .col-2 {float: none !important;width: 100% !important;}</style>
    <?php
};
add_action( 'woocommerce_checkout_before_customer_details', 'custom_shipping_css_styles' );
```