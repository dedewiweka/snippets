## Remove editor from templates
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Tweaks/remove-editor-from-templates.md) 
```php
add_action('admin_head', 'remove_editor_from_page');
function remove_editor_from_page() {
  if(isset($_GET['post'])) {
		$id = $_GET['post'];
		$template = get_post_meta($id, '_wp_page_template', true);

		if($template = 'page-template.php') {
			remove_post_type_support('page', 'editor');
		}
	}
}
```