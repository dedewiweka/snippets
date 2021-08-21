## Woocommerce Make Full Width Billing Field

### Code Snippet

```markdown
//MAKE BILLING FIELD WIDTH 100%
function custom_billing_css_styles() {
    ?>
<style>
.woocommerce .col2-set .col-1, .woocommerce-page .col2-set .col-1 {float: none !important;width: 100% !important;}

</style>
    <?php
};
add_action( 'woocommerce_checkout_before_customer_details', 'custom_billing_css_styles' );
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).
