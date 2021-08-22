## Display reuseable block in theme
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Blocks/display_reusable_block_in_theme.md) 
```php
// Post ID of your reusable block (find in Manage Reusable Blocks)
$id = 25;
$reusable_block = get_post($id);
echo apply_filters('the_content', $reusable_block->post_content);
```
