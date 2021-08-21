## Change number of products per row

### Code Snippet

```php
add_filter('loop_shop_columns', 'my_loop_columns');
if(!function_exists('my_loop_columns')) {
	function my_loop_columns() {
		return 3;
	}
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).