## Custom RSS footer

### Code Snippet

```php
add_filter('the_excerpt_rss', 'my_postrss');
add_filter('the_content', 'my_postrss');
function my_postrss($content) {
  if(is_feed()){
    $content .= 'This is my custom RSS footer.';
  }
  return $content;
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).