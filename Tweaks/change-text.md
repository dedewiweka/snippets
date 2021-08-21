## Change text

### Code Snippet

```php
add_filter('gettext', 'my_string_replace');
function my_string_replace($text) {
  $text = str_replace('Old', 'New', $text);
  return $text;
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).