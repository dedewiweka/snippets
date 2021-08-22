## Disable RSS
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Security/disable-rss.md) 
```php
add_action('do_feed', 'disable_rss_feed', 1);
add_action('do_feed_rdf', 'disable_rss_feed', 1);
add_action('do_feed_rss', 'disable_rss_feed', 1);
add_action('do_feed_rss2', 'disable_rss_feed', 1);
add_action('do_feed_atom', 'disable_rss_feed', 1);
function disable_rss_feed() {
    wp_die('Sorry, no RSS feed available. Please try at our <a href="' . get_bloginfo('url') . '">homepage</a>.');
}
```