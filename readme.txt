=== Plugin Name ===
Contributors: MartyThornley, mindshare
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=11225299
Tags: php, browser detection, browser, internet explorer, iphone, mobile, browscap, detection
Version: 2.2
Tested up to: 3.6-beta1
Stable tag: 2.2

PHP Browser Detection is a WordPress plugin used to detect a user's browser. This version 2.2 is a fairly big update so please report any bugs.

== Description ==

PHP Browser Detection is a WordPress plugin used to detect a user's browser. It can be used to send conditional CSS files for Internet Explorer, display different content or custom messages anywhere on the page, or to swap out Flash for an image for iPhones.

**Using the Template Tags in your theme:**

*Test for specific browsers:*

$version is optional. Include a major version number, a single integer - 3,4,5, etc... Or leave it empty to test for any version.

`<?php if(is_firefox($version)) { /* do stuff */ }; ?>`

`<?php if(is_safari($version)) { /* do stuff */ }; ?>`

`<?php if(is_firefox($version)) { /* do stuff */ }; ?>`

`<?php if(is_chrome($version)) { /* do stuff */ }; ?>`

`<?php if(is_opera($version)) { /* do stuff */ }; ?>`

`<?php if(is_ie($version)) { /* do stuff */ }; ?>`

*Check for mobile, iPhone, iPad, iPod, etc...*

`<?php if(is_iphone($version)) { /* do stuff */ }; ?>`

`<?php if(is_ipad($version)) { /* do stuff */ }; ?>`

`<?php if(is_ipod($version)) { /* do stuff */ }; ?>`

`<?php if(is_mobile()) { /* do stuff */ }; ?>`

*Check for greater than / less then a specific version...*

Less than or equal to Firefox 19:
`<?php if(is_firefox() && get_browser_version() >= 19) { /* do stuff */ }; ?>`

Less than or equal to IE 10:
`<?php if(is_ie() && get_browser_version() < 10) { /* do stuff */ }; ?>`

Greater than or equal to Safari 4:
`<?php if(is_safari() && get_browser_version() > 4) { /* do stuff */ }; ?>`

these are just a few examples, but this syntax will work for any browser or version.

*Check specific versions...*

Is the browser IE6?
`<?php if(is_ie(6)) { /* do stuff */ }; ?>`

Is the browser IE10?
`<?php if(is_ie(10)) { /* do stuff */ }; ?>`

**Or you can get all the info and do what you want with it:**

*Get just the name...*

`<?php $browserName = get_browser_name(); ?>`

Get the full version number - 3.2, 5.0, etc...

`<?php $browserVersion = get_browser_version(); ?>`

*Or get it all in array...*

`<?php $browserInfo = php_browser_info(); ?>`

== Installation ==

1. Automatically install through the Plugin Browser or...
1. Upload entire `php-browser-detection` folder to the `/wp-content/plugins/` directory.
1. Activate the plugin through the 'Plugins' menu in WordPress.

Or with MU / MultiSite:

1. Add `php-browser-detection.php` and `php_browser_detection_browscap.ini` to `mu-plugins` to make sure every blog has it auto activated.

== Changelog ==

= 2.2 =
* updated php_browser_detection_browscap.ini to version 5020 (custom version)
* minor code cleanup
* added tests.php to check all plugin features
* added additional usage examples to readme.txt
* deprecated is_ie9() functions in favor is is_ie(9), etc.
* fixed issue with is_ipod
* fixed issue with is_mobile
* fixed issue with detecting Android 4.2.*
* fixed issue with boolean values
* other minor bug fixes reported on wordpress.org

= 2.1.3 =
* updated php_browser_detection_browscap.ini to version 5016

= 2.1.2 =

* updated php_browser_detection_browscap.ini to version 5004

= 2.1.1 =

* updated php_browser_detection_browscap.ini to version 4911

= 2.1 =

* fixed path info to work with 'mu-plugins' folder, version 2.0 didn't know how to find it.
* better recognition of iPad and iPhone with iOS 4

= 2.0 =

* Added tests for iPad, iPod, Chrome, Opera
* Added ability to test for any version for each browser
* Added ability to get browser name and get browser version

= 1.2 =

* fixed the lesser than statements.
* They had been looking for lesser than or equal to
* Fixed the is_safari() statement.

= 1.1 =
* Fixed error on line 156 preventing activation

