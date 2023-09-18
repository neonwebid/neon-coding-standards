# Shortcode Development
## Basic Shortcode Knowledge
@see https://developer.wordpress.org/apis/shortcode/

## Shortcode Tricky Tips
**Render HTML On Shortcode**
```php
...

add_shortcode('render_html_mode', 'callback_template');

function callback_template() {
    ob_start();
    .... html code ...
    
    return ob_get_clean();
}
...

```