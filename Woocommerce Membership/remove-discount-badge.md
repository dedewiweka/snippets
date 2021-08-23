## Woocommerce Membership Remove Discount Badge
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce%20membership/remove-discount-badge.md) 
```php
//Remove discount badge
add_filter( 'wc_memberships_member_discount_badge', '__return_empty_string' );
```