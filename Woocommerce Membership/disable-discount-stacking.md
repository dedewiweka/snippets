## Woocommerce Membership Disable Discount Stacking
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce%20membership/disable-discount-stacking.md) 
```php
//Disable Discount Stacking for member
add_filter( 'wc_memberships_allow_cumulative_member_discounts', '__return_false' );
```