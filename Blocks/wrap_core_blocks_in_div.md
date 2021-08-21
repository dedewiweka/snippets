## Wrap blocks in div

### Code Snippet

```php
add_filter('render_block', 'my_render_block', 10, 2);
function my_render_block($block_content, $block) {
  if(strpos($block['blockName'], 'core/') !== false) {
		$block_content = '<div class="my-custom-class">' . $block_content . '</div>';
  }
  
  return $block_content;
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).