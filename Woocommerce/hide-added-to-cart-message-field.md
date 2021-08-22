## Woocommerce Hide Added To Cart Message Field

### Code Snippet

```php
//HIDE ADDED TO CART MESSAGE FIELD
	add_filter( 'wc_add_to_cart_message', 'remove_add_to_cart_message' );
	function remove_add_to_cart_message() {
		return;
	}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).
