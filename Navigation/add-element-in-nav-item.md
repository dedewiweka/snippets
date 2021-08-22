## Add element in navigation item
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Navigation/add-element-in-nav-item.md) 
```php
add_filter('walker_nav_menu_start_el', 'my_add_custom_element');
function my_add_custom_element($item_output, $item, $depth, $args) {
  return '<span>My custom element</span>';
}
```