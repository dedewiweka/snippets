## Restrict access to post type

### Code Snippet

```php
add_action('template_redirect', 'my_restrict_access_to_post_type');
function my_restrict_access_to_post_type() {
  $post_type = 'my_custom_post_type';
  $user_role = 'admin'
  $login_page = esc_url(home_url('/login-path'));

  if(is_singular($post_type) || is_post_type_archive($post_type)) {
    if(!is_user_logged_in() && !current_user_can($user_role)) {
      wp_redirect($login_page);
    }
  }
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).