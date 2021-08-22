## Logout link
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Users/log-out-link.md) 
```php
// With security confirmation 
?>
<a href="<?php echo esc_url(home_url('/wp-login.php?action=logout')); ?>">
  <?php _e('Log out', 'text_domain'); ?>
</a>
<? php;
```
```php
// Without security confirmation
?>
<a href="<?php echo wp_logout_url(); ?>">
  <?php _e('Log out', constant('THEME\TEXT_DOMAIN')); ?>
</a>
<? php;
```