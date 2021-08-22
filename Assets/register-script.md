## Register scripts
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/register-script.md) 
```php
add_action('init', 'my_enqueue_assets');
function my_enqueue_assets() {
  wp_register_script('myscript', get_theme_file_uri('/assets/js/myscript.js'));
  wp_enqueue_script('myscript', get_template_directory_uri() . '/assets/js/myscript.js', array('jquery'), '1', true);
}
```