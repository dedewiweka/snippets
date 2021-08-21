## Add element in navigation item

### Code Snippet

```php
add_filter('walker_nav_menu_start_el', 'my_add_custom_element');
function my_add_custom_element($item_output, $item, $depth, $args) {
  return '<span>My custom element</span>';
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).