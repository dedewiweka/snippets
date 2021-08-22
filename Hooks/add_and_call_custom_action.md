## Snippet title
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Hooks/add_and_call_custom_action.md) 
```php
// In functions.php - Add custom action hook
add_action('my_action_hook', 'my_action_function');
function my_action_function() {
  echo 'Do your stuff';
}
```
```php
// In template files - Do action if it wasn't called before in the theme
if(did_action('my_action_hook') === 0) do_action('my_action_hook');
```