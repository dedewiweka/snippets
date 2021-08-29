## Add user role
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Users/add-user-role.md) 
```php
add_role('user_role_name', __('User Role Name', 'text_domain'), array(
    'read'            => true,
    'create_posts'    => false,
    'edit_posts'      => false
  )
);
```
