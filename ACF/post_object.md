## Post object

### Code Snippet

```markdown
$post_obj = get_field('my_post_obj');
if(!empty($post_obj)) {
  global $post;
  $post = $post_obj;
  setup_postdata($post);
  /**
   * Insert markup
   */
  wp_reset_postdata();
}
```
### Explanations
- Explain briefly how the snippet works.
- Use bullet points for the snippet's explanation.
- Try to explain everything briefly but clearly.

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).