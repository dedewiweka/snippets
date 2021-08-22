## Woocommerce Make Full Width Shipping Field
### Code Snippet

```php
//MAKE FULL WIDTH SHIPPING FIELD
function custom_shipping_css_styles() {
    ?>
<style>.woocommerce .col2-set .col-2, .woocommerce-page .col2-set .col-2 {float: none !important;width: 100% !important;}</style>
    <?php
};
add_action( 'woocommerce_checkout_before_customer_details', 'custom_shipping_css_styles' );
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).
