## Remove admin bar

### Code Snippet

```php
add_action('after_setup_theme', 'my_remove_admin_bar');
function my_remove_admin_bar() {
  if(!(current_user_can('administrator') && is_admin())) {
    show_admin_bar(false);
  }
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).