WP Github Activity
==================

Wordpress plugin for showing github user activity from a post, page, template or widget.

## Usage
### Shortcode
```
[github_activity user="A7M2" limit=5 cache=300]
```
- `user` The github login name whose activity list you wish to show. Default value: `A7M2`
- `limit` The maximum number of lines you wish to show (up to 30). Default value: `5`
- `cache` The number of seconds the api data should be cached (0 for no cache). Default value: `300` (5 minutes)

### Widget
Simply navigate to `http://yoursite.com/wp-admin/widgets.php` to set up the widget!

### Template tag
```php
get_github_user_activity( $user = 'A7M2', $limit = 5, $cache = 300 )
```
- `$user` The github login name whose activity list you wish to show
- `$limit` The maximum number of lines you wish to show (up to 30)
- `$cache` The number of seconds the api data should be cached (0 for no cache)

Examples:
```php
// shows the five most recent github user activities for user A7M2
echo get_github_user_activity( 'A7M2' );
// shows only the latest github user activity for user A7M2
echo get_github_user_activity( 'A7M2', 1 );
// shows only the latest github user activity for user A7M2 without caching the results
echo get_github_user_activity( 'A7M2', 1, 0 );
```

## Languages
The default language for this plugin is English, but there's also a Dutch translation available. 
You can add your own .mo files to the plugin's `language/` directory, or use another plugin such as WPML to translate WP GitHub Activity.

For help with adding your own languages, please read this article http://www.foxrunsoftware.net/articles/wordpress/translating-a-wordpress-plugin-step-by-step/
