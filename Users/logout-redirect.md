## Logout redirect

### Code Snippet

```php
add_action('wp_logout', 'my_redirect_after_logout');
function my_redirect_after_logout() {
  wp_redirect(esc_url(home_url('/')));
  exit;
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).