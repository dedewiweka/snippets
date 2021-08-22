## Wrap blocks in div
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Blocks/wrap_core_blocks_in_div.md) 
```php
add_filter('render_block', 'my_render_block', 10, 2);
function my_render_block($block_content, $block) {
  if(strpos($block['blockName'], 'core/') !== false) {
		$block_content = '<div class="my-custom-class">' . $block_content . '</div>';
  }
  
  return $block_content;
}
```