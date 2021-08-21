## Register style in plugin

### Code Snippet

```php
add_action('init', 'my_enqueue_plugin_assets');
function my_enqueue_plugin_assets()
{
    wp_register_style('mystyle', get_theme_file_uri('/assets/css/mystyle.css'));
    wp_enqueue_style('mystyle');
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