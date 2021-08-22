## Check on activations
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Plugins/check-on-activation.md) 
```php
register_activation_hook(__FILE__, 'my_activate_plugin');
function my_activate_plugin() {
  //Check if current version of WP is compatible with the plugin
  if(version_compare(bloginfo('version'), '4.5', '<')) {
    wp_die(__('Please update your Wordpress installation to use this plugin.'), 'plugin');
  }
}
```