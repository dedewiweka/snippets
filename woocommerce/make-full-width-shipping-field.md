## Woocommerce Make Full Width Shipping Field

### License

[GNU General Public License v3.0](https://github.com/dedewiweka/projects/blob/main/license)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).


### Code Snippet

```markdown
//MAKE FULL WIDTH SHIPPING FIELD
function custom_shipping_css_styles() {
    ?>
<style>.woocommerce .col2-set .col-2, .woocommerce-page .col2-set .col-2 {float: none !important;width: 100% !important;}</style>
    <?php
};
add_action( 'woocommerce_checkout_before_customer_details', 'custom_shipping_css_styles' );
```