## Blocks

### Code Snippet

```php
// Inside functions.php ?>
  // Register testimonial block
  add_action('acf/init', 'my_acf_init');
  function my_acf_init() {
    if(function_exists('acf_register_block')) {
      $args = array(
        'name'				    => 'testimonial',
        'title'				    => __('Testimonial', 'text_domain'),
        'description'		  => __('This is my custom testimonial block', 'text_domain'),
        'render_callback'	=> 'my_acf_render_testimonial_block',
        'category'			  => 'formatting',
        'icon'            => 'admin-comments',
        'keywords'        => array('testimonial', 'quote')
      );
      acf_register_block($args);
    }
  }

  // Render testimonial block
  function my_acf_render_testimonial_block($block) {
    // Convert name to path friendly slug
    $slug = str_replace('acf/', '', $block['name']);

    // Include a template part from the 'template-parts/block folder
    if(file_exists(get_theme_file_path('/template-parts/block/content-' . $slug . '.php'))) {
      include(get_theme_file_path(('/template-parts/block/content-' . $slug . '.php')));
    }
  }

  // Block name: Testimonial

  // Get ACF fields
  $avatar = get_field('avatar');
  $testimonial = get_field('testimonial');
  $author = get_field('author');
  $background_color = get_field('background_color');
  $text_color = get_field('text_color');

  // Create ID attr for specific styling
  $id = 'testimonial-' . $block['id'];

  // Create align class alignwide from block setting wide
  $align_class = $block['align'] ? 'align' . $block['align'] : '';
?>

<style>
  #<?php echo $id; ?> {
    background-color: <?php echo $background_color; ?>;
    color: <?php echo $text_color; ?>;
  }
</style>

<blockquote 
  id="<?php echo $id; ?>"
  class="testimonial <?php echo $align_class; ?>"
>
  <p><?php echo $testimonial; ?></p>
  <cite>
    <img 
      src="<?php echo $avatar['url']; ?>" 
      alt="<?php echo $avatar['alt']; ?>"
    >
    <span><?php echo $author; ?></span>
  </cite>
</blockquote>
```
### Explanations
- Explain briefly how the snippet works.
- Use bullet points for the snippet's explanation.
- Try to explain everything briefly but clearly.

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).