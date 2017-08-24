```
  ________________      ________                      
 /_  __/ ____/ __ \_  _/_  __/ /_  ___  ____ ___  ___ 
  / / / __/ / / / / |/_// / / __ \/ _ \/ __ `__ \/ _ \
 / / / /___/ /_/ />  < / / / / / /  __/ / / / / /  __/
/_/ /_____/_____/_/|_|/_/ /_/ /_/\___/_/ /_/ /_/\___/ 
                                                      
```

# TEDxTheme

This theme has been designed and coded by [The Working Group](http://twg.ca) and [TEDxToronto](http://www.tedxtoronto.com) and modified by [Alex Justesen](http://alexjustesen.com) in the hopes that other TEDx organizations will find this easy to use to promote and manage their own events.

### Requirements

* **PHP 5.4** or greater
* **MySQL 5.0** or greater
* The **mod_rewrite** Apache module
* A recent version of **WordPress**

### Installation (Production)
* Download the latest theme release [TEDx Theme](https://github.com/alexjustesen/TEDxSpringfieldTheme/releases)
* Install the following WordPress plugins dependencies:
    * [Advanced Custom Fields](http://www.advancedcustomfields.com/)
    * [Option Tree](https://wordpress.org/plugins/option-tree/)

### Installation (Developers)

* Clone/fork or download the latest repo zip from (https://github.com/alexjustesen/TEDxSpringfieldTheme) and install it to `./wp-content/themes/`.
* Run `npm install`
* Run `bower install`
* Run `gulp default`
* Install the following WordPress plugins dependencies:
    * [Advanced Custom Fields](http://www.advancedcustomfields.com/)
    * [Option Tree](https://wordpress.org/plugins/option-tree/)


### Development

We've done our best to setup an efficient workflow using [Gulp.js](http://gulpjs.com/) and [Bower](http://bower.io/). You'll need to have `npm` installed before getting started. Development requires an understanding of the following commands:

* `npm install` - Install development dependencies.
* `bower install` - Install packages to `./vendor` directory.
* `gulp default` - Is the default Gulp function that compiles and moves all the site assets to the `./dist` directory.
* `gulp clean` - Cleans out the build and dist folders.
* `gulp package` - Packages the WordPress Theme zip file.
* `gulp vendor-js vendor-css` - Concats and minifies Bower dependencies into a single `vendor.min.js` and `vendor.min.css` file. These dependencies are declared in the `Gulpfile.js`. To add a new plugin install it with Bower and then declare it in the gulp file.


### Change Log

#### v1.1.0 (in development)
- Added: `dollarshaveclub/shave` package to bower for text truncation
- New: Video card design for featured/past talks
- New: Header design to include social links for Facebook, Instagram and Twitter
- New: Moved call to action button/text to large section below the header
- New: Created a new call to action button/text for app download
- New: Navigation bar and menu walker
- Changed: Gulp `build` to `package` to handle creating the theme zip file
- Fixed: `.gitirnore` to exclude the `./vendor` directory
- Fixed: Gulp `images` function to move all images for frontend and admin
- Fixed: Gulp `clean`, was referencing an invalid directory
- Fixed: Gulp `fonts`, was missing reference to Bootstrap fonts
- Fixed: logo anchor to use `home_url()` instead of a custom function
- Removed: DNS prefetch from `header.php` in favor of using a plugin
- Removed: Twitter button and widget JS from `footer.php`
- Removed: Facebook sdk from `header.php`
- Removed: WP customize option for twitter button code
- Removed: Support for AngularJS
- Removed: Selective menu walker
- Removed: Gulp `watch` function
- Updated: `.gitignore` to include the `vendor` directory
- Updated: jQuery package to v3.2.1

#### v1.0.2 (Oct 3, 2016)
- Corrected the team member placeholder in `includes/custom_post_types/team.php`
- Corrected the text at the bottom of `footer.php` to meet the TEDx guidelines
- Removed link to the legal notice in `footer.php`

#### v1.0.1 (Sept 30, 2016)
- Removed reference to http protocol in `shortcode_templates/talk_shortcode.php` to support http and https
- Updated `screenshot.png` to match current theme preview

#### v1.0.0 (Sept 23, 2016)
- Forked from TEDxTheme and renamed to TEDxSpringfieldTheme
- Removed TWG and Jet Cooper images from `footer.php`
- Added Built by 'Alex Justesen' to `footer.php`
- Removed banner text and button from `page_templates/template_home.php`
- Removed speaker video preview from `shortcode_templates/speaker_card_shortcode.php`
- Removed related speaker video preview from `sidebar-speaker.php`
- Removed http protocol from YouTube preview image from `shortcode_templates/talk_shortcode.php` to support http and https protocols