## Disable comments
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/Security/disable-comments.md) 
```php
//Disable support for comments and trackbacks in post types
add_action('admin_init', 'disable_comments_post_types_support');
function disable_comments_post_types_support() {
    $post_types = get_post_types();
        foreach ($post_types as $post_type) {
            if(post_type_supports($post_type, 'comments')) {
                remove_post_type_support($post_type, 'comments');
                remove_post_type_support($post_type, 'trackbacks');
            }
    }
}
```
```php
//Close comments on the front-end
add_filter('comments_open', 'disable_comments_status', 20, 2);
add_filter('pings_open', 'disable_comments_status', 20, 2);
function disable_comments_status() {
    return false;
}
```
```php
//Hide existing comments
add_filter('comments_array', 'disable_comments_hide_existing_comments', 10, 2);
function disable_comments_hide_existing_comments($comments) {
    $comments = array();
    return $comments;
}
```
```php
//Remove comments page in menu
add_action('admin_menu', 'disable_comments_admin_menu');
function disable_comments_admin_menu() {
    remove_menu_page('edit-comments.php');
}
```
```php
//Redirect any user trying to access comments page
add_action('admin_init', 'disable_comments_admin_menu_redirect');
function disable_comments_admin_menu_redirect() {
    global $pagenow;
    if ($pagenow === 'edit-comments.php') {
        wp_redirect(admin_url()); exit;
    }
}
```
```php
//Remove comments metabox from dashboard
add_action('admin_init', 'disable_comments_dashboard');
function disable_comments_dashboard() {
    remove_meta_box('dashboard_recent_comments', 'dashboard', 'normal');
}
```
```php
//Remove comments links from admin bar
add_action('init', 'disable_comments_admin_bar');
function disable_comments_admin_bar() {
    if (is_admin_bar_showing()) {
        remove_action('admin_bar_menu', 'wp_admin_bar_comments_menu', 60);
    }
}
```