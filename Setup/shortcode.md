## Shortcode 
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Setup/shortcode.md) 
```php
//Basic Shortcode
add_shortcode('shortcode_name', 'shortcode_function');
function shortcode_function() {
    $output = 'Put something here.';
    return $output;
}
```
```php
//Shortcode with atts
add_shortcode('atts_shortcode', 'my_atts_shortcode');
function my_atts_shortcode($atts, $content = null) {
  $atts = shortcode_atts(
    array(
      'attribute'	=>	'value'
    ),
    $atts,
    'atts_shortcode'
  );

  return '<div class="' . $atts['attribute'] . '">' . $content . '</div>';
}
```
```php
//Shortcode with content
add_shortcode('content-shortcode', 'my_content_shortcode');
function($atts, $content = null) {
  return '<div class="my-content-wrapper">' . $content . '</div>';
}
```