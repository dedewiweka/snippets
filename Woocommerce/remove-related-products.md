## Remove related products
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/remove-related-products.md) 
```php

remove_action('woocommerce_after_single_product_summary', 'woocommerce_output_related_products', 20);

```