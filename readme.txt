=== Referrer Detector ===
Contributors: Phoenixheart
Donate link: http://www.phoenixheart.net/wp-plugins/referrer-detector/
Tags: referrer, detector, greetings, greet box, social
Requires at least: 2.2
Tested up to: 3.2.1
Stable tag: 4.2.1.0

Helps your blog detect where the user comes from and automatically displays the corresponding greetings.

== Description ==
This plugin displays a greeting message to visitors that come from different urls (known as *referrers*). For example, you may want to welcome Diggers with a message that reminds them to digg your story, or you may want to ask Del.icio.us users to bookmark your post, and so on.

Not only about a cool greeting box, it greatly helps to more efficiently interacts with your readers and build a better relationship between you (your website) and them.

== Features ==
* A pure AJAXed admin interface with elements tidily divided into tabs. Entries can be added/modified/(de)activated/deleted without the need to reload the entire page, or even with just one click. Starting from 3.2, there are even bulk actions!
* The greet box position can be set to before, after, or (starting from 3.2) both before and after the post. A [custom tag](http://www.phoenixheart.net/2008/11/referrer-detector/#custom_tag) can also be used in case you don't want to show greetings on every post.
* Users can also put a tag (`<?php if (function_exists('referrer_detector')) referrer_detector(); ?>`) into the template to show the greet box anywhere of choice.
* Excluded URLs can be specified in order to hide the greet box from specific users (like ones from Google Reader).
* A * wildcard character can be used in both referrers and excluded URLs. For example: google.* will apply for all localized Google domains.
* Multiple URLs can be merged into one entry, seperated by commas. For example: del.icio.us,delicious.com.
* Ability to include WordPress attributes like url, title, author, category etc. into the greetings.
* A STAT panel to get data reporting about the visitor statistic.
* Many installed-by-default entries (which can be restored anytime with one click). Upon installing, you will have these entries available:
	1. 9 rules
	1. Bing
	1. BuySellAds
	1. Del.icio.us and Delicious.com
	1. Digg
	1. Gizmodo
	1. Google
	1. Lifehacker
	1. Live Search
	1. Reddit
	1. StumbleUpon
	1. TechCrunch
	1. Technograti
	1. TechRadar
	1. Twitter
	1. Yahoo!
* Compatible with caching plugins, since the core is written and run in JavaScript which is normally not cached.
* Automatically detect user's country and display the localized greetings (if any).
* Ability to backup and restore entries, excluded URLs, and options, very convenient for transferring between sites.
* Welcome box now can be shown in lightbox style using [SimpleModal](http://www.ericmmartin.com/projects/simplemodal/) jQuery plugin.
* Optimized OOP code allows extreme readability and easy modifications for other plugin developers.

== Installation ==
As usual:

1. Download the plugin
1. Extract into a folder
1. Upload the entire to `wp-content/plugins/` directory of your WordPress installation
1. Enable it via Plugins panel
1. It should now work out of the box. If you want to tweak a bit, head to Settings->Referrer Detector

== Frequently Asked Questions ==
= It just doesn't work! =
Sorry to hear that. Try deactivate and then reactivate it. Saving the options may sometimes work.
If things are still bad, please buzz me with more information, like under what circumstances, what are your settings etc. If it's a bug I will try to fix it.

= Will it work with my cache plugin? =
It should - just make sure you delete the cache right after plugin activation. Normally, a cache plugin only caches the server content as a static HTML file. As Referrer Detector uses client-side JavaScript, it should work regardless if the page is cached or not. If in any case it doesn't work with a specific caching plugin, please let me know.

= How do I change the default icon? I'm sick of that RSS thing! =
The default icon file is wp-content/plugins/referrer-detector/images/icons/default.png. Re-decorate it however you want.

= How about the CSS styles of the greeting box? =
You can modify /wp-content/plugins/referrer-detector/css/style.css but it's NOT recommended, as the changes will be lost with each upgrade. Instead, create /wp-content/plugins/referrer-detector-style.css, copy the content from /wp-content/plugins/referrer-detector/css/style.css, and start modifying. Upon starting up, Referrer Detector will check if /wp-content/plugins/referrer-detector-style.css exists first, and use it if it does.

= The default RSS link is incorrect! My feed is served through FeedBurner! =
Oops... I'm sorry. The default RSS link is automatically retrieved from your WordPress settings, so I can't have any idea about your FeedBurner url. In this case I'm afraid you'll have to update the default entries manually... well, until I find another way around this.

= I place the PHP code `if (function_exists('referrer_detector')) referrer_detector(); ` into my theme. Now the author and category tags won't turn into proper values anymore? =
This should happen if you place the code in the index.php file, and your home page is showing multiple posts/excerpts. In such a case the plugin don't know which post to retrieve those author and category data from, so it decides to get only the common data available: the page URL and title.

= Is there a limit to the number of entries (referrers)? =
Virtually no. However, as the entries data is saved into a javascript file, too many entries will make that file bloated, and this may affect your page's loading speed.

= I messed the entries up! How can I restore the default entries back? =
Version 2.1 introduces this feature already. Use it wisely though, as it's a one-way action.

= How does the "merge entries" feature work? =
The selected entries' URLs will be merged into one, seperated by commas. Other information (icon, name, greeting text) is taken from the oldest entry. In fact they should be the same (so that merging makes sense) so there should be no problem.

= Why is an "explode entry" not available? =
I doubt there's a need to explode one entry into seperated ones... but if commonly requested, I will implement it.

= Why does the plugin sometimes detect wrong country and give the wrong localized message? =
The country detection relies from HostIP.info service. For this reason, if the service fails to indicate the correct country, my plugin fails to give the correct message.

= Where did you get the icons? =
Instead of grabbing them from [FastIcon](http://fasticon.com/freeware/index.php/web-2-social-bookmark-icons/), I did them myself for my own sake :) If you want to create more icons with the same style, [here](http://www.phoenixheart.net/wp-stuffs/referrer-detector-icon.psd) is the original PSD file.

= Just curious, how did you test this plugin? You don't have back links from all of those referrers, yes? =
Of course I don't - I'm not that famous. Instead, I use the great [Firebug](http://www.getfirebug.com/) to inspect and modify a link on those sites to link to my post, and there I have a good referrer ;) If you have a better and quicker solution, please let me know.

= I like this plugin. How do I support its development? =
Thank you! Please consider putting a link back to [my blog](http://www.phoenixheart.net). And please note - the initial credits go to [Thaya Kareeson](http://omninoggin.com) and his great [WP Greet Box plugin](http://omninoggin.com/projects/wordpress-plugins/wp-greet-box-wordpress-plugin/).

== Screenshots ==
1. The entry list
2. Add a new entry
3. Edit an existing entry
4. Excluded URLs
5. Generic Options
6. STAT
7. The plugin in action - to 9rules users
8. The plugin in action - to Diggers
9. The plugin in action - to Stumblers

== History ==
* 4.2.1.0
1. Temporarily removed Backup/Restore feature for security reasons.
* 4.2.0.3
1. Add Bing and BuySellAds entries. You can either reset the entries or create on your own using the new icons inside referrer-detector/images/icons/ directory
1. Deleting the plugin now removes all options and data - Don't try it ;)
1. Several fixes and enhancements
* 4.2.0.2 Raise compatibility
* 4.2.0.1
1. Added an option to display the welcome box in light box style
1. Fixed several IE bugs
* 4.1.0 
1. Welcome box CSS rewritten
1. Added ability to optionally display related posts
* 4.0.1 - A hot fix attempting to fix allow_call_time_pass_reference problem
* 4.0
1. Completely rewritten code - now optimized OOP
1. Data are now stored in database for better security
1. Introduced the ability to backup entries, excluded URLs, options (you can choose from these 3)
1. Introduced the ability to add localized messages to welcome user visiting from different countries.
1. STATs reporting is now using Google Chart
* 3.2
1. Introduced Bulk Actions
1. Supported wildcard (asterisk character) in both referrers and excluded URLs, for example google.* matches all Google domains.
1. Introduced the ability to merge several URLs into one entry, seperated by commas. For example: del.icio.us,delicious.com
1. The greeting box can now be place BOTH before and after a post.
1. Some minor graphic changes and bug fixes.
* 3.1
1. Fix the javascript bug on IE that prevents the greeting box from being shown up.
1. The javascript files are now [minified](http://www.crockford.com/javascript/jsmin.html) instead of [packed](http://dean.edwards.name/packer/) to improve performance.
* 3.0.2 Made a mistake in 3.0.1
* 3.0.1 Fixed the bug that made the home page XHTML invalid
* 3.0 Added the Stats panel. Now the plugin can show (customizable) stats of visits from different referrers from time to time.
* 2.2.0.1 Fixed the javascript bug when jQuery library is not included by default.
* 2.2 Added ability to include search terms into the greet box. Supports almost all common search engines.
* 2.1.1 A small fixed on form serialization and a (possible) security flaw.
* 2.1 A minor release, introducing the ability to restore the entries to default.
* 2.0 Second major release, which has some important changes:
1. A much much clearer admin interface with tabs, along with some enhancements.
1. An option to *not* show the greeting box for visitors that come from specified URLs ("excluded" ones), for example Google Reader. The list can be edited easily via admin panel.
1. Users can now put a tag (`<?php if (function_exists('referrer_detector')) referrer_detector(); ?>`) into the template to show the greet box.
1. Some javascript files are packed to save bandwidth and loading time.
* 1.2 Several important fixes and improvements.
1. Fixed the bug when multiple greet boxes are shown if the page is filled with multipe full posts (such as homepage).
1. Fixed the bug in the initial SQL data where the default RSS feed url is set to mine (tooo bad I forgot to check it).
1. Fixed the javascript error when the page has no referrer.
1. Update the installation and FAQ section.
1. And some little stuffs...
* 1.1 Better support to work with cache plugins. Now the generic options take effect without the need to delete the cache.
* 1.0.1 A quick fix for caching problem (if cache is enabled and the first user has no referrer, the plugin will fail).
* 1.0 Initial version