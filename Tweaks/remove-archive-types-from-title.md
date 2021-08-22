## Remove archieve types from title
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Tweaks/remove-archive-types-from-title.md) 
```php
add_filter('get_the_archive_title', 'lt_remove_archive_types_from_titles');
function lt_remove_archive_types_from_titles($title) {
	if (is_category()) {
		$title = single_cat_title('', false);
	} elseif (is_tag()) {
		$title = single_tag_title('', false);
	}
	
	return $title;
}
```