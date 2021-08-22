## Insert term
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Terms/insert-term.md) 
```php
add_action('init', 'add_my_cats');
function add_my_cats() {
  
  if(!term_exists('Term name', 'term-parent')) {
    wp_insert_term(
      'Term name',
      'term-parent',
      array(
        'description' =>  'My term description',
        'slug'        =>  'term-name'
      )
    );
  }

}
```