## Add option page

### Code Snippet

```markdown
if(function_exists('acf_add_options_page') && function_exists('acf_add_options_sub_page')) {
    $args = array(
        'page_title'    =>  'My ACF Options Page',
        'menu_title'    =>  'My ACF Options Page',
        'menu_slug'     =>  'my_acf_options_page',
        'icon_url'      =>  'dashicons-admin-site'
    );
    acf_add_options_page($args);
}
```
### Explanations
- Explain briefly how the snippet works.
- Use bullet points for the snippet's explanation.
- Try to explain everything briefly but clearly.

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).