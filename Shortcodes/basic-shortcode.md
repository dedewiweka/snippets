## Add Shortcode

### Code Snippet

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
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).