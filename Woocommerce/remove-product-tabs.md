## Remove product tabs
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/remove-product-tabs.md) 
```php
add_filter('woocommerce_product_tabs', 'my_remove_product_tabs');
function my_remove_product_tabs($tabs) {
  unset($tabs['description']);
  unset($tabs['reviews']);
  unset($tabs['additional_information']);

  return $tabs;
}
```