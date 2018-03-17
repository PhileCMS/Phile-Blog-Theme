Phile-Blog-Theme
================

This is a theme developed to showcase how blogging works on [Phile](https://github.com/PhileCMS).

### Disclaimer

Please use a fresh Phile installation in order to avoid errors not associated with this theme/demo.

### Installation

First, [download this repo](https://github.com/james2doyle/Phile-Blog-Theme/archive/master.zip) and drop the folder into the root directory that Phile was installed into.

The following changes need to be made to your config.php file in order for this theme to work normally:

```php
…
// set the theme for this installation
$config['theme'] = 'blog';

// set some defaults for the pages
$config['date_format'] = 'jS F, Y'; // 11th November, 2013
$config['pages_order'] = 'meta.date:desc'; // this is a blog so date ordering

return $config;
```
