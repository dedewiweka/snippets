## Custom RSS footer
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/RSS/custom-rss-footer.md) 
```php
add_filter('the_excerpt_rss', 'my_postrss');
add_filter('the_content', 'my_postrss');
function my_postrss($content) {
  if(is_feed()){
    $content .= 'This is my custom RSS footer.';
  }
  return $content;
}
```