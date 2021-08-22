## Snippet title
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Security/remove-version-number.md) 
```php
//Remove version number
remove_action('wp_head', 'wp_generator');
add_filter('the_generator', '__return_empty_string');
```
```php
//Remove version number from styles and scripts
add_filter('style_loader_src', 'remove_script_version', 999);
add_filter('script_loader_src', 'remove_script_version', 999);
function remove_script_version($src) {
    if(strpos($src, '?ver=') || strpos($src, 'ver=')) {
        $src = remove_query_arg( 'ver', $src );
    }
    return $src;
}
```