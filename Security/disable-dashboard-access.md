## Disable dashboard access
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Security/disable-dashboard-access.md) 
```php
add_action('admin_init', 'my_disable_dashboard_access');
function my_disable_dashboard_access() {
  if(!current_user_can('manage_options') && $_SERVER['DOING_AJAX'] != '/wp-admin/admin-ajax.php') {
    wp_redirect(esc_url(home_url('/')));
    exit;
  }
}
```