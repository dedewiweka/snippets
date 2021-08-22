## Remove product tabs

### Code Snippet

```php
add_filter('woocommerce_product_tabs', 'my_remove_product_tabs');
function my_remove_product_tabs($tabs) {
  unset($tabs['description']);
  unset($tabs['reviews']);
  unset($tabs['additional_information']);

  return $tabs;
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).
