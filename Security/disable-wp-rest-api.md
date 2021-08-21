## Disable WP REST API

### Code Snippet

```php
add_filter('rest_authentication_errors', 'disable_my_endpoints');
function disable_my_endpoints() {
    if(!is_user_logged_in()) {
        return new WP_Error('rest_cannot_access', 'Access denied', array('status' => rest_authorization_required_code()));
    }
    return $access;
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).