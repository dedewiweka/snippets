## Multiple navigation menus

### Code Snippet

```php
add_action('after_setup_theme', 'my_theme_setup');
function my_theme_setup() {
	$menus = array(
		'main'		=>	__('Main Menu', 'text-domain'),
		'sitemap'	=>	__('Sitemap', 'text-domain'),
		'privacy'	=>	__('Privacy', 'text-domain'),
		'social'	=>	__('Social Networks', 'text-domain')
	);
  register_nav_menus($menus);
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).
