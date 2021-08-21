## Woocommerce Membership Disable Discount Stacking

### Explanations
- Useful to disable discount stacking on woocommerce membership plugin.
- Discount stacking could happen when user have several membership plan

### Code Snippet

```markdown
//Disable Discount Stacking for member
add_filter( 'wc_memberships_allow_cumulative_member_discounts', '__return_false' );
```
### License

[GNU General Public License v2.0](https://github.com/dedewiweka/snippets/blob/main/LICENSE)


### Support and Contact

For more information and details about my work please visit [My Development Website](https://dede.wiweka.com/development).
