## Snippet title

### Code Snippet

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
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).