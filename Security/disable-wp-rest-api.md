## Disable WP REST API
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Security/disable-wp-rest-api.md) 
```php
add_filter('rest_authentication_errors', 'disable_my_endpoints');
function disable_my_endpoints() {
    if(!is_user_logged_in()) {
        return new WP_Error('rest_cannot_access', 'Access denied', array('status' => rest_authorization_required_code()));
    }
    return $access;
}
```