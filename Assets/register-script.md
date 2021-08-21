## Register scripts

### Code Snippet

```php
add_action('init', 'my_enqueue_assets');
function my_enqueue_assets() {
  wp_register_script('myscript', get_theme_file_uri('/assets/js/myscript.js'));
  wp_enqueue_script('myscript', get_template_directory_uri() . '/assets/js/myscript.js', array('jquery'), '1', true);
}
```
### Explanations
- Explain briefly how the snippet works.
- Use bullet points for the snippet's explanation.
- Try to explain everything briefly but clearly.

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).