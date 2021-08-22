## Disable prefetching
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Tweaks/disable-prefetching.md) 
```php
remove_action('wp_head', 'adjacent_posts_rel_link_wp_head', 10, 0);
```