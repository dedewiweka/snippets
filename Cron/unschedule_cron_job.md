## Unschedule cron job

### Code Snippet

```php
add_action('init', function() {

  $time = wp_next_schedule('my_cron_hook');
  wp_unschedule_event($time, 'my_cron_hook');

  if(!wp_next_scheduled('my_cron_hook')) {
    wp_schedule_event(time(), 'hourly', 'my_cron_hook');
  }
});
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).