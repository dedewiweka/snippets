## Add custom scheduling
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Cron/add_custom_schedulling.md) 
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