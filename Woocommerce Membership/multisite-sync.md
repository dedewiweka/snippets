## Multisite Sync
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce%20Membership/multisite-sync.md) 
```php
add_filter('query', function($query) { global $wpdb;

if (strpos($query, 'wc_membership') !== false) { $query = str_replace($wpdb->prefix, 'main_website_prefix', $query); } return $query; });
```
