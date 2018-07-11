# Setting up a Development Environment

## Why set up a development environment?

When developing themes, it is best to do it in an environment identical to the production server which will eventually host your WordPress installation.  Your development environment can either be local or remote.  Configuring a local environment to work on your WordPress theme is beneficial for several reasons:

* You can build your theme locally without relying on a remote server. This speeds up your development process and allows you to see changes instantly in your browser.
* You do not need an Internet connection to build your theme.
* You can test your theme from a variety of perspectives. This is important, especially if you plan on releasing your theme to a larger audience and want to ensure maximum compatibility.


## Your WordPress local development environment

For developing WordPress themes, you need to set up a development environment suited to WordPress.  To get started, you will need a local server stack and a text editor.  There are a number of options, including:

**Local Server Stack**

* A local server stack, such as LAMP (Linux Apache MySQL/MariaDB PHP) or WAMP (Windows Apache MySQL/MariaDB PHP) is a server (much like the server that runs on your web server), which you will configure on your local machine. You can install pre-bundled programs that contain all of these, like MAMP (for Mac), or XAMPP (Mac or Windows) to quickly setup your environment.

**Virtualized Environment**

* A virtualized such created with Vagrant and VirtualBox allows you to create easily reproducible development environments. Varying Vagrant Vagrants (VVV) is a popular Vagrant option which creates a WordPress development environment.

**Text Editor**

* In addition to a local server environment, you also need a text editor to write your code. Your choice of text editor is personal, but remember that a good text editor can speed up your development process. Your text editor can be everything from a basic tool for writing code to a fully integrated development environment (IDE) with tools for debugging and testing. It’s worth doing research, and some even include support for WordPress development. Popular choices are Atom, Sublime Text, and PhpStorm.

You can find a list of tutorials for setting up development environments at the bottom of the page.

## Supporting older versions of WordPress

It’s standard practice for WordPress themes to support at least two versions back to ensure a minimum of backward compatibility. For example, if the current version of WordPress is at 4.6, then you should also make sure that your theme works well in versions 4.5 and 4.4 as well.

You can refer to the [WordPress Roadmap](https://wordpress.org/about/roadmap/) page to access older versions of WordPress. Then you can download and install older WordPress versions, creating multiple development sites, each running different WordPress versions for testing.

## WP_DEBUG

Configuring debugging is an essential part of WordPress theme development. WordPress provides a number of constants to support your debugging efforts. These includes:

**WP_DEBUG**

The [WP_DEBUG](https://codex.wordpress.org/WP_DEBUG) PHP constant is used to trigger the built-in “debug” mode on your WordPress installation. This allows you to view errors in your theme. To enable it:

1. Open your WordPress installation’s wp-config.php file

2. Change:


    define( 'WP_DEBUG', false );

to

    define( 'WP_DEBUG', true );


> Note: While normally set to ‘false’ in the wp-config.php file, development copies of WordPress—alpha and beta versions of the upcoming release—WP_DEBUG is already set to ‘true’ by default.

**WP_DEBUG_DISPLAY and WP_DEBUG_LOG**

[WP_DEBUG_LOG](https://codex.wordpress.org/Debugging_in_WordPress#WP_DEBUG_LOG) and [WP_DEBUG_DISPLAY](https://codex.wordpress.org/Debugging_in_WordPress#WP_DEBUG_DISPLAY) are additional PHP constants which extend WP_DEBUG.

WP_DEBUG_LOG is used in conjunction with WP_DEBUG to log all error messages to a debug.log within your WordPress /wp-content/ directory. To enable this functionality set WP_DEBUG_LOG to true within your wp-config.php file.

    define( 'WP_DEBUG_LOG', true );

WP_DEBUG_DISPLAY is used to control whether debug messages display within the HTML of your theme pages. To display error messages on the screen as they occur, configure this setting to ‘true’ within your wp-config.php file.

    define( 'WP_DEBUG_DISPLAY', true );

With the WP_DEBUG and WP_DEBUG_DISPLAY enabled, error messages will display at the top of your site pages.

![admin-sample-debug](https://developer.wordpress.org/files/2014/07/admin-sample-debug.png)

> Note: Errors will display in the frontend and admin areas of your site.These debug tools are meant for local testing and staging installs, not for live sites.

## Other WordPress Development Tools

In addition to WP_DEBUG, the following plugins and unit test data sets are an important part of your [development toolset](http://nacin.com/2010/04/23/5-ways-to-debug-wordpress/) and help you develop better WordPress themes.

### Test Data

**WordPress.org Theme Unit Test Data**

[WordPress.org Theme Unit Test Data](https://codex.wordpress.org/Theme_Unit_Test) is an XML file containing dummy test data that you can upload to test how themes perform with different types and layouts of content.

**WordPress.com Theme Unit Test Data**

[WordPress.com Theme Unit Test Data](http://themetest.wordpress.com/) is dummy test data that you can upload to a WordPress installation to test your theme, including WordPress.com-specific features.

### Plugins

**Debug Bar (WordPress plugin)**

[Debug Bar](https://wordpress.org/plugins/debug-bar/) adds an admin bar to your WordPress admin providing a central location for debugging.

**Query Monitor (WordPress plugin)**

[Query Monitor](https://wordpress.org/plugins/query-monitor/) allows debugging of database queries, API request and AJAX called used to generate theme pages and theme functionality.

**Log Deprecated Notices (WordPress plugin)**

[Log Deprecated Notices logs](https://wordpress.org/plugins/log-deprecated-notices/) incorrect function usage and the use of deprecated files and functions in your WordPress theme.

**Monster Widgets (WordPress plugin)**

[Monster Widget](https://wordpress.org/plugins/monster-widget/) consolidates the core WordPress widgets into a single widget allowing you to test widgets styling and functionality in your theme.

**Developer (WordPress plugin)**

[Developer](https://wordpress.org/plugins/developer/) helps optimize your development environment by allowing easy installation of tools and plugins that help in troubleshooting and ensuring code quality.

**Theme-Check (WordPress plugin)**

[Theme-Check](https://wordpress.org/plugins/theme-check/) tests your theme for compliance with the latest WordPress standards and practices.


## WordPress Theme Review Guidelines

In addition to the above development tools, it’s a good idea to stay up to date on the WordPress.org Theme Review Team’s [Guidelines](https://make.wordpress.org/themes/guidelines/) for theme submission and guidance on meeting [WordPress Coding Standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/).  These guidelines are the “gold standard” for quality theme development and are useful, even if you don’t plan on releasing a theme on WordPress.org.

## Further Resources

* [Developing WordPress Locally With MAMP](http://www.smashingmagazine.com/2011/09/28/developing-wordpress-locally-with-mamp/) (Mac, MAMP)
* [How to Setup a WordPress Development Environment for Windows](http://code.tutsplus.com/articles/how-to-setup-a-wordpress-development-environment-for-windows--wp-23365) (Windows, XAMPP)
* [WordPress Theme Review VVV: A Quick Vagrant Setup for Testing Themes](http://wptavern.com/wordpress-theme-review-vvv-a-quick-vagrant-setup-for-testing-and-reviewing-themes) (Cross-platform, Vagrant)
* [Setting up your Development Environment](http://vip.wordpress.com/documentation/development-environment/) (WordPress.com VIP)
* [wptest.io](http://wptest.io/) – an exhaustive set of WordPress test data derived from [WordPress’ Theme Unit Test](https://codex.wordpress.org/Theme_Unit_Test)
