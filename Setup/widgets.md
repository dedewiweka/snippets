## Widgets
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Setup/widgets.md) 
```php
add_action('widgets_init', 'my_widgets');
function my_widgets() {
  register_sidebar(array(
    'name'          =>  __('My Widget', 'mytheme'),
    'id'            =>  'my_widget',
    'description'   =>  __('My Simple Widget', 'mytheme');
    'before_widget' =>  '<section class="my-widget">',
    'after_widget'  =>  '</section>',
    'before_title'  =>  '<h3 class="my-widget-title">',
    'after_title'   =>  '</h3>'
  ));
}
```