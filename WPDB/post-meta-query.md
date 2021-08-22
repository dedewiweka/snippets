## Snippet title

### Code Snippet

```php
global $wpdb;
$meta_query = "
    SELECT $wpdb->postmeta.meta_value 
    FROM $wpdb->postmeta 
    WHERE $wpdb->postmeta.meta_key = 'my_meta_key'
";
$meta_data = $wpdb->get_results($meta_query, OBJECT);
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).