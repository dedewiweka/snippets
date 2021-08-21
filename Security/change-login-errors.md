## Change login errors

### Code Snippet

```php
add_filter('login_errors', 'no_login_errors');
function no_login_errors() {
    return 'Something went wrong. Please try again!';
}
```
### Explanations

### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)

### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).
