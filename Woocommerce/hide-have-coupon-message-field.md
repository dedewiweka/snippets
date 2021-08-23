## Woocommerce Hide Have Coupon Message Field
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/hide-have-coupon-message-field.md) 
```php
// HIDE HAVE COUPON MESSAGE FIELD
remove_action( 'woocommerce_before_checkout_form', 'woocommerce_checkout_coupon_form', 10 ); 
```