## Woocommerce Membership Disable Discount Stacking

### License

[GNU General Public License v3.0](https://github.com/dedewiweka/projects/blob/main/license)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).


### Code Snippet

```markdown
//Disable Discount Stacking for member
add_filter( 'wc_memberships_allow_cumulative_member_discounts', '__return_false' );
```