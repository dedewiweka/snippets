## Insert term

### Code Snippet

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
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).