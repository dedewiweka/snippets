## Woocommerce Membership Remove Discount Badge

### License

[GNU General Public License v3.0](https://github.com/dedewiweka/projects/blob/main/license)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).


### Code Snippet

```markdown
//Remove discount badge
add_filter( 'wc_memberships_member_discount_badge', '__return_empty_string' );
```