## Check on activations

### Code Snippet

```php
register_activation_hook(__FILE__, 'my_activate_plugin');
function my_activate_plugin() {
  //Check if current version of WP is compatible with the plugin
  if(version_compare(bloginfo('version'), '4.5', '<')) {
    wp_die(__('Please update your Wordpress installation to use this plugin.'), 'plugin');
  }
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).