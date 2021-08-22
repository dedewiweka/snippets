## Gallery
[![License](https://img.shields.io/github/license/dedewiweka/snippets?color=brightgreen)](https://github.com/dedewiweka/snippets/blob/main/LICENSE) [![Contact](https://img.shields.io/badge/contact-Dede%20Wiweka-orange)](https://dede.wiweka.com/development) ![File size](https://img.shields.io/github/size/dedewiweka/snippets/gallery.md) 
```php
  $gallery = get_field('my_gallery');
  if($gallery);
?>
  <div class="my-gallery">
    <ul>
      <?php foreach($gallery as $image) : ?>
        <li>
          <a href="<?php echo $image['url']; ?>" class="my-gallery-item" alt="<?php echo $image['alt']; ?>">
            <img src="<?php echo $image['sizes']['medium']; ?>" alt="<?php echo $image['alt']; ?>">
          </a>
        </li>
      <?php endforeach; ?>
    </ul>
  </div><!-- /.my-gallery -->
<?php endif; ?>
```