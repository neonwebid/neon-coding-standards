# NEON: Coding Standards For WordPress Development

## Development Knowledge Base
- [Basic Coding Standard](basic-coding-standard.md)
- [Security Improving](security.md)
- [Shortcode Development](shortcode.md)

## Development Requirement
- set `WP_DEBUG` TRUE `wp-config.php`
- use `register_shutdown_function( callback )` to catch un showing error

```
register_shutdown_function( function() {
    print_r( error_get_last() );
});
```

## Hooks
### Hook Action
Use ``add_action($hook_name, $callback, $priority = 10, $number_args = 1)`` <br>
@see https://developer.wordpress.org/plugins/hooks/actions/

Action Hook @see https://codex.wordpress.org/Plugin_API/Action_Reference

### Hook Filter
Use ``add_filter($hook_name, $callback, $priority = 10, $number_args = 1)`` <br>
@see https://developer.wordpress.org/plugins/hooks/filters/ <br>

Filter Hook @see https://codex.wordpress.org/Plugin_API/Filter_Reference