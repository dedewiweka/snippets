## Delay posts
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/RSS/delay-posts.md) 
```php
add_filter('posts_where', 'my_delay_posts');
function my_delay_posts($where) {
  global $wpdb;

  if(is_feed()) {
    // Get timestamp & set delay
    $now = gmdate('Y-m-d H:i:s');
    $wait = '10';
    $device = 'MINUTE' // MINUTE, HOUR, DAY, WEEK, MONTH, YEAR

    // Add to default SQL WHERE
    $where .= " AND TIMESTAMPDIFF($device, $wpdb->posts.post_date_gmt, '$now') > $wait ";
  }

  return $where;
}
```