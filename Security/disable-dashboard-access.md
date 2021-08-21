## Disable dashboard access

### Code Snippet

```php
add_action('admin_init', 'my_disable_dashboard_access');
function my_disable_dashboard_access() {
  if(!current_user_can('manage_options') && $_SERVER['DOING_AJAX'] != '/wp-admin/admin-ajax.php') {
    wp_redirect(esc_url(home_url('/')));
    exit;
  }
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).
