## Format date

### Code Snippet

```markdown
$date = get_field('date_picker_field');

$format_in = 'Ymd';
$format_out = 'd.m.Y.';
$formatted_date = DateTime::createFromFormat($format_in, $date);

echo $formatted_date->format($format_out);
```
### Explanations
- Explain briefly how the snippet works.
- Use bullet points for the snippet's explanation.
- Try to explain everything briefly but clearly.

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).