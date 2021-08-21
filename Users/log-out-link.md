## Logout link

### Code Snippet

```php
// With security confirmation 
<a href="<?php echo esc_url(home_url('/wp-login.php?action=logout')); ?>">
  <?php _e('Log out', 'text_domain'); ?>
</a>
```
```php
// Without security confirmation
<a href="<?php echo wp_logout_url(); ?>">
  <?php _e('Log out', constant('THEME\TEXT_DOMAIN')); ?>
</a>
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).