## Remove first and last class

### Code Snippet

```php
add_filter('post_class', 'my_prefix_post_class', 21);
function my_prefix_post_class($classes) {
	if('product' == get_post_type() && is_search()) {
		$classes = array_diff($classes, array('first', 'last'));
	}
	return $classes;
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).