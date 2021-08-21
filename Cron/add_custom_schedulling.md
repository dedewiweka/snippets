## Add custom scheduling

### Code Snippet

```php
add_action('init', function() {
  if(wp_next_scheduled('my_cron_hook')) {
    wp_schedule_event(time(), 'hourly', 'my_cron_hook');
  }
});

add_action('my_cron_hook', function() {
  // Triggered actions go here
});

add_filter('cron_schedules', function($schedules) {
  $schedules['five-minutes'] = array(
    'interval'  =>  300,
    'display'   =>  'Every Five Minutes'
  );

  return $schedules;
});
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).