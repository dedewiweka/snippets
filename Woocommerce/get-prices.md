## GET Price

### Code Snippet

```php
$currency = get_woocommerce_currency_symbol();
$price = get_post_meta(get_the_ID(), '_regular_price', true);
$sale = get_post_meta(get_the_ID(), '_sale_price', true);

if($sale) : 

?>
  <span><?php echo $sale . $currency;?></span>
<?php elseif($price) : ?>
  <span><?php echo $price . $currency; ?></span>
<?php 
  endif;
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).


