## Display reuseable block in theme

### Code Snippet

```php
// Post ID of your reusable block (find in Manage Reusable Blocks)
$id = 25;
$reusable_block = get_post($id);
echo apply_filters('the_content', $reusable_block->post_content);
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).