## Custom admin footer
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Tweaks/custom-admin-footer.md) 
```php
add_filter('admin_footer_text', 'my_custom_admin_footer');
function my_custom_admin_footer() {
  echo 'This is my custom admin footer.';
}
```