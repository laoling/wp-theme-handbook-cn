# Main Stylesheet (style.css)

The style.css is a stylesheet (CSS) file required for every WordPress theme. It controls the presentation (visual design and layout) of the website pages.

## Location

In order for WordPress to recognize the set of theme template files as a valid theme, the style.css file needs to be located in the root directory of your theme, not a subdirectory.

For more detailed explanation on how to include the style.css file in a theme, see the “Stylesheets” section of Enqueuing Scripts and Styles.

## Basic Structure

WordPress uses the header comment section of a style.css to display information about the theme in the Appearance (Themes) dashboard panel.

### Example

Here is an example of the header part of style.css.

        /*
        Theme Name: Twenty Seventeen
        Theme URI: https://wordpress.org/themes/twentyseventeen/
        Author: the WordPress team
        Author URI: https://wordpress.org/
        Description: Twenty Seventeen brings your site to life with immersive featured images and subtle animations. With a focus on business sites, it features multiple sections on the front page as well as widgets, navigation and social menus, a logo, and more. Personalize its asymmetrical grid with a custom color scheme and showcase your multimedia content with post formats. Our default theme for 2017 works great in many languages, for any abilities, and on any device.
        Version: 1.0
        License: GNU General Public License v2 or later
        License URI: http://www.gnu.org/licenses/gpl-2.0.html
        Text Domain: twentyseventeen
        Tags: one-column, two-columns, right-sidebar, flexible-header, accessibility-ready, custom-colors, custom-header, custom-menu, custom-logo, editor-style, featured-images, footer-widgets, post-formats, rtl-language-support, sticky-post, theme-options, threaded-comments, translation-ready
        This theme, like WordPress, is licensed under the GPL.
        Use it to make something cool, have fun, and share what you've learned with others.
        */

Items indicated with (*) are required for a theme in the WordPress Theme Repository.

> Note: WordPress Theme Repository uses the number after “Version” in this file to determine if the theme has a new version available.

* Theme Name (*): Name of the theme.
* Theme URI: The URL of a public web page where users can find more information about the theme.
* Author (*): The name of the individual or organization who developed the theme. Using the Theme Author’s wordpress.org username is recommended.
* Author URI: The URL of the authoring individual or organization.
* Description (*): A short description of the theme.
* Version (*): The version, written in X.X or X.X.X format.
* License (*): The license of the theme.
* License URI (*): The URL of the theme license.
* Text Domain (*): The string used for textdomain for translation.
* Tags: Words or phrases that allow users to find the theme using the tag filter. A full list of tags is in the Theme Review Handbook.
* Domain Path: Used so that WordPress knows where to find the translation when the theme is disabled. Defaults to /languages.

After the required header section, style.css can contain anything a regular CSS file has.

## Style.css for a Child Theme

If your theme is a Child Theme, the Template line is required in style.css header.

      /*
      Theme Name: My Child Theme
      Template: Twenty Seventeen
      */

For more information on creating a Child Theme, visit the Child Themes page.
