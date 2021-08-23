## Set default ordering
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/set-default-ordering.md) 
```php
add_filter('woocommerce_default_catalog_orderby', 'my_custom_default_ordering');
function my_custom_default_ordering() {
  return 'your-peferred-ordering';
}
```