## GET Price
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Woocommerce/get-prices.md) 
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