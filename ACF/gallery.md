## Gallery

### Code Snippet

```markdown 
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
### Explanations
- Explain briefly how the snippet works.
- Use bullet points for the snippet's explanation.
- Try to explain everything briefly but clearly.

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).
