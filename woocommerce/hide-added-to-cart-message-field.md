## Woocommerce Hide Added To Cart Message Field

### License

[GNU General Public License v3.0](https://github.com/dedewiweka/projects/blob/main/license)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).


### Code Snippet

```markdown
//HIDE ADDED TO CART MESSAGE FIELD
	add_filter( 'wc_add_to_cart_message', 'remove_add_to_cart_message' );
	function remove_add_to_cart_message() {
		return;
	}
```
