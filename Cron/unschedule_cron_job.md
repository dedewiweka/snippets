## Unschedule cron job
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Cron/unschedule_cron_job.md) 
```php
add_action('init', function() {

  $time = wp_next_schedule('my_cron_hook');
  wp_unschedule_event($time, 'my_cron_hook');

  if(!wp_next_scheduled('my_cron_hook')) {
    wp_schedule_event(time(), 'hourly', 'my_cron_hook');
  }
});
```