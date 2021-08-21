## Disable RSS

### Code Snippet

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
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).