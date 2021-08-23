## Loop through taxonomies
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/WP%20Query/loop-through-taxonomies.md) 
```php
$taxonomies = get_terms(array(
  'taxonomy'      => 'tax-slug',
  'orderby'       => 'term_id',
  'order'         => 'ASC'
));

foreach($taxonomies as $tax) {
  $args = array(
    'post_type'         => 'custom_post_type',
    'tax_query'         => array(
      array(
        'taxonomy'      => 'tax-slug',
        'field'         => 'slug',
        'terms'         => array($tax->slug),
        'operator'      => 'IN'
      )
    )
  );

  $tax_query = new WP_Query($args);

  echo '<h2>' . $tax->name . '</h2>';

  if($tax_query->have_posts()) {
    while($tax_query->have_posts()) {
      $tax_query->the_post();

      the_title();
    }
  }

  $tax_query = null;
  wp_reset_postdata();
}
```