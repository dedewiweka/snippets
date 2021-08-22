## Change text
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Tweaks/change-text.md) 
```php
add_filter('gettext', 'my_string_replace');
function my_string_replace($text) {
  $text = str_replace('Old', 'New', $text);
  return $text;
}
```