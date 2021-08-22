## Add option page
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/add-options-page.md) 
```php
if(function_exists('acf_add_options_page') && function_exists('acf_add_options_sub_page')) {
    $args = array(
        'page_title'    =>  'My ACF Options Page',
        'menu_title'    =>  'My ACF Options Page',
        'menu_slug'     =>  'my_acf_options_page',
        'icon_url'      =>  'dashicons-admin-site'
    );
    acf_add_options_page($args);
}
```