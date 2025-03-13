# WordPress Useful Commands / Scripts

### Generate multiple WooCommerce Coupon Codes from terminal, command line, wp cli, wc cli
`wp wc shop_coupon create --amount='150' --discount_type='fixed_cart' --date_expires='EXAMPLE DATE FORMAT 2023-12-31' --usage_limit='1' --usage_limit_per_user='1' --exclude_sale_items=false --individual_use=true --user=1 --code='INSERT CODE' --description='INSERT DESCRIPTION'`


```
// Disable auto-update success emails for WordPress plugins updates
add_filter( 'auto_plugin_update_send_email', 'wp_stop_plugins_update_emails', 10, 4 );
function wp_stop_plugins_update_emails( $enabled, $update_results ) {
    if ( ! empty( $type ) && 'success' === $type ) {
        return false;
    }
    return true;
}

// Disable auto-update success emails for WordPress core updates
add_filter( 'auto_core_update_send_email', 'wp_stop_core_update_emails', 10, 4 );
function wp_stop_core_update_emails( $send, $type, $core_update, $result ) {
    if ( ! empty( $type ) && 'success' === $type ) {
        return false;
    }
    return true;
}
```
