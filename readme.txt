=== QuickShare ===
Contributors: celloexpressions
Tags: Social, Share, Sharing, Social Sharing, Social Media, Quick, Lightweight, No JS, Flexible, Customizable, Facebook, Twitter, Pinterest, Linkedin, Google+, Tumblr, Email, Reddit, StumbleUpon
Requires at least: 3.5
Tested up to: 3.6
Stable tag: 1.0
Description: Add quick social sharing functions to your content. Challenge social sharing norms with a flexible design and fast performance.
License: GPLv2

== Description ==
This plugin, like many others, adds content-sharing functions after your posts (and optionally pages and media attachments). But the similarities end there. 

QuickShare is quick because it doesn't run 3rd-party sharing JavaScript; in fact, there is **no** front-end JS. The sharing functions are built into links that take the user (in new tabs) to the native sharing interface on each social media site.

You can choose which social media sites to include from: Facebook, Twitter, Pinterest, Linkedin, Google+, Tumblr, Reddit, and StumbleUpon. A basic email function is also available.

The share bar appearance is highly customizable and share functions can be displayed as either icons, Genericons or text. Each display method features different customization options; customize through the settings page or with custom CSS.

As a bonus, QuickShare includes several built-in CSS3 effects for hover state animations.

*Please visit the plugin support forum for help with custom css snippets and/or feature requests.*

== Installation ==
1. Take the easy route and install through the WordPress plugin adder OR
1. Download the .zip file and upload the unzipped folder to the `/wp-content/plugins/` directory
1. Activate the plugin through the 'Plugins' menu in WordPress
1. Configure the settings in Settings -> QuickShare
1. Make sure that your theme has the `wp_head()` action hook and uses `the_content()`; this is where QuickShare hooks into. Alternately, add `<?php do_quickshare_output(); ?>` to your template files.

== Frequently Asked Questions ==
= Optimizing Pinterest Sharing (and images) =
Pinterest is image-centric, so any content to be shared via Pinterest should include an image. QuickShare attempts to find an image in each post by first looking for a featured image, then grabbing the first attached image, looking for a raw image tag, or finally falling beck to a site-wide default image that you can set. You can also hide Pinterest sharing if no post image is found. The post image will also be used for Facebook sharing, by default.

= Customizing the Social Share Images =
QuickShare provides many options for design customization, but if you want to go as far as changing the share images (if Genericons aren't working for you either), you can! Just throw in some custom CSS, based on the code in `quickshare.css`. You could even use your own icon font in place of Genericons!

= Using Custom CSS Styling =
If you look at quickshare.css, you'll notice that the majority of the plugin's options are controlled through CSS. I recommend poking around in there to get some ideas, then adding your styles to the custom CSS field in the admin settings page. Placing the code here will ensure it overrides all plugin options. Depending on the share display type (icons/genericons/text), you can change icon and background colors and sizes, adjust shadows and borders, change how the plugin fits with your theme's layout (margins, padding, horizontal separations), add more CSS3 effects, and more! Unfortunately, it will be necessary to use `!important` in some places.

= Share bar doesn't display =
QuickShare can only display after posts use `the_content()`. One example of where QuickShare can't display is in gallery post formats on index and archive (not single view) pages in the Twenty Thirteen theme. However, if you have a custom theme or a child theme, you can customize the QuickShare output by adding `<?php do_quickshare_output(); ?>` to your template files somewhere within the loop.

For additional customization, you can use `<?php do_quickshare_output( $url, $title, $source, $description, $imgurl ); ?>`, where `$url` is the link to the content to share, `$title` is the title, `$source` is the name of your website/blog, `$description` is a short description, and `$imgurl` is the thumbnail image url. This version of the custom QuickShare output can be used anywhere in your templates, inside or outside of the loop, opening the door to many customization options. If any of the parameters are null, QuickShare will attempt to populate them with the default values (using the `$post` global).

= Browser Support =
QuickShare is designed for modern browsers. I do not (and will not make much effort to) support IE8 or below, and do not support features that aren't achievable with minimal CSS in other outdated browsers (including, now, IE9). That being said, if you find a compatibility issue *with an easy fix*, let me know on the support forums and I'll consider including it. In the meantime, you can always add any desired CSS to the custom CSS field without worrying about losing plugin edits to updates. For the most part, everything should fail gracefully; older browsers won't see special effects like rounded corners, transitions/animations, box shadows, and opacity filters, but will be functionally fine. Genericons do not work in several browsers (including IE7/8 and IE9 mobile, but not IE9 desktop), so don't use that display option if you need lots of browser support.

= Genericons are Different Sizes and Styles =
I know. I didn't design Genericons (an icon font originally created for the Twenty Thirteen theme). They were designed as different sizes, so that's just how they are (I think this design decision is related to the fun quirkiness of Genericons and Twenty Thirteen). They need to be sized at multiples of 16 for best results, so there's no good way to compensate for the discrepancies. If it bothers you, just use one of the other display options! You can probably use your own icon font with QuickShare and custom CSS too, if you want.

= Icons are missing for Reddit and Stumbleupon =
Well, the Genericons are actually missing and it's because there aren't Genericons for either icon (see above). Depending on who you ask, these sites are less popular and on the way out, but I included them in the plugin with partial support in case anyone really wants them.

= Sharing to additional social media networks =
If you think QuickShare should support sharing to additional networks, please let me know in the support forums and I'll consider adding support. I don't intend to add any more networks that would be enabled by default (or automatically enabled after an update), though.

= WordPress Version Support =
QuickShare does **not** work in WordPress versions below 3.5 (it will probably throw a php fatal error when attempting to activate). For best results, always use the latest version of WordPress.


== Screenshots ==
1. Admin settings screen with live preview of output (with MP6).
2. Default plugin display with the Twenty Thirteen theme.

== Changelog ==
= 1.0 =
* First publically available version of the plugin.
* Compatible with WordPress 3.5-3.6

== Upgrade Notice ==
= 1.0 =
* Initial public release