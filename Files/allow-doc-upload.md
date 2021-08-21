## Allow doc upload

### Code Snippet

```php
add_filter('upload_mimes','my_add_custom_mime_types');
function my_add_custom_mime_types($mimes) {
	return array_merge($mimes,array(
		'doc' => 'application/msword',
		'docx' => 'application/vnd.openxmlformats-officedocument.wordprocessingml.document'
	));
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).