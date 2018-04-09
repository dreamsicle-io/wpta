# WPGulp

A simple, zero configuration Gulp build &amp; lint setup for developing modern WordPress themes. This setup will build and optimize SASS, JavaScript, language localizations, and images. 

Unlike many WP x Gulp build setups, this one is built entirely on Gulp 4, and will only bundle assets (`.js`, `.css`) and language files (`.pot`). This setup will also create the required style.css file and its formatted header comment, as well as a repository-friendly `README.md` file; all generated by the theme root's `package.json` data.

The package also includes a php class named `WPGulp` in `class-wpgulp.php`. This class beautifully handles script and stylesheet enqueues of built assets automatically. 

## File structure

This gulp setup has zero configuration, however it does expect that your project root's package.json is setup properly, and that an oppinionated file structure is followed. The localization tasks are handled by the built in WordPress i18n functions in all theme `.php` files, but the source assets should be structured accordingly.

### Source Files

```
root
―――― /assets
―――― ―――― /src
―――― ―――― ―――― /js
―――― ―――― ―――― ―――― /modules
―――― ―――― ―――― ―――― site.js
―――― ―――― ―――― ―――― admin.js
―――― ―――― ―――― ―――― customizer.js
―――― ―――― ―――― /sass
―――― ―――― ―――― ―――― /modules
―――― ―――― ―――― ―――― site.scss
―――― ―――― ―――― ―――― admin.scss
―――― ―――― ―――― ―――― editor.scss
―――― ―――― ―――― /images
```

### Build Files

```
root
―――― /assets
―――― ―――― /dist
―――― ―――― ―――― /js
―――― ―――― ―――― ―――― site.min.js
―――― ―――― ―――― ―――― site.min.js.map
―――― ―――― ―――― ―――― admin.min.js
―――― ―――― ―――― ―――― admin.min.js.map
―――― ―――― ―――― ―――― customizer.min.js
―――― ―――― ―――― ―――― customizer.min.js.map
―――― ―――― ―――― /css
―――― ―――― ―――― ―――― site.min.css
―――― ―――― ―――― ―――― site.min.css.map
―――― ―――― ―――― ―――― admin.min.css
―――― ―――― ―――― ―――― admin.min.css.map
―――― ―――― ―――― ―――― editor.min.css
―――― ―――― ―――― ―――― editor.min.css.map
―――― ―――― ―――― /images
―――― /languages
―――― ―――― {textdomain}.pot
―――― README.md
―――― style.css
```
