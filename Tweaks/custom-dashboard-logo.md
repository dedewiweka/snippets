## Custom dashboard logo
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Tweaks/custom-dashboard-logo.md) 
```php
add_action('wp_before_admin_bar_render', 'my_custom_logo');
function my_custom_logo() {
  echo '
    <style type="text/css">
      #wpadminbar #wp-admin-bar-wp-logo > .ab-item .ab-icon:before {
        background-image: url(' . get_bloginfo('stylesheet_directory') . '/assets/images/logo.png) !important;
        background-position: 0 0;
        color:rgba(0, 0, 0, 0);
      }
      #wpadminbar #wp-admin-bar-wp-logo.hover > .ab-item .ab-icon {
        background-position: 0 0;
      }
    </style>
  ';
}
```