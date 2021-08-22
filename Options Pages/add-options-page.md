## Add options page
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Options%20Pages/add-options-page.md) 
```php
add_action('admin_menu', 'my_options_page');
function my_options_page() {
  $page_title = 'Options page';
	$menu_title = 'Options page';
	$capability = 'manage_options';
	$slug = 'my_options';
	$callback = 'my_options_content';
	$icon = 'dashicons-clipboard';
  $position = 100;
  
  add_menu_page($page_title, $menu_title, $capability, $slug, $callback, $icon, $position);
}

function my_options_content() {
?>
  <div class="wrap">
    <h1>This is my options page</h1>
  </div><!-- /.wrap -->
<?php 
}
```