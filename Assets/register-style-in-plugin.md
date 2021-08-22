## Register style in plugin
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/register-style-in-plugin.md) 
```php
add_action('init', 'my_enqueue_plugin_assets');
function my_enqueue_plugin_assets()
{
    wp_register_style('mystyle', get_theme_file_uri('/assets/css/mystyle.css'));
    wp_enqueue_style('mystyle');
}
```