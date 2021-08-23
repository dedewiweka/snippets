## Create custom tables
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/WPDB/create-custom-tables.md) 
```php
add_action('init', 'my_create_custom_tables');
function my_create_custom_tables () {
  global $wpdb;
  $charset_collate = $wpdb->get_charset_collate();
  $table_name = $wpdb->prefix . 'my_website_terms';
  $sql = "CREATE TABLE IF NOT EXISTS $table_name (
      id mediumint(9) NOT NULL AUTO_INCREMENT,
      entry_name char(20) NOT NULL,
      term_term datetime DEFAULT '0000-00-00 00:00:00' NOT NULL,
      PRIMARY KEY (id)
    ) $charset_collate";
  require_once( ABSPATH . 'wp-admin/includes/upgrade.php' );
  dbDelta( $sql );
}
```