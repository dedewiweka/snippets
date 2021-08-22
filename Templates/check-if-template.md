## Check if template
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Templates/check-if-template.md) 
```php
$template = get_post_meta($id, '_wp_page_template', true);

if($template == 'page-contact.php') {
// Break stuff
}
```