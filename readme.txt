=== Remove Cookies From Static Resources ===
Contributors: giuse
Donate link: buymeacoffee.com/josem
Requires at least: 4.6
Tested up to: 6.5
Stable tag: 0.0.1
Requires PHP: 5.6
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html
Tags:  cleanup, performance

It removes cookies from the requests to static resources for the modern browsers.


== Description ==

It removes cookies from the requests to static resources for modern browsers.

When the browser requests a static resource such as an image, a stylesheet, or a script, it sends to the server all the cookies, and it does it at every request.
If your page requests 10 scripts, then it sends 10 times the cookies.
As you have probably heard, a way to solve this issue is to serve the static resources from a cookies-free subdomain.
The cookies-free subdomain is a possible solution, but sometimes you have no wish to create a subdomain only for the static assets and give instructions to WordPress for fetching them from the subdomain.

Moreover, why don't we solve this issue directly at the root? Is the browser that sends cookies to the server, so let's address this issue with the browser.
This is exactly what Remove Cookies From Static Resources does. It instructs the browser to don't send its cookies when it requests static resources.
However, this solution will work only with the modern browsers that support the crossorigin attribute.
The plugin simply adds crossorigin="anonymous" to all the requested scripts, links, and images. Nothing else.
This plugin will not work for old browsers. It will also not work for all those resources that are added with JavaScript, or CSS.

This plugin has no settings. No additional HTTP requests, no additional database queries. It consumes practically zero.

You should see an improvement in performance if yor website requests many static resources sending big data through the cookies.
In all other cases you don't need this plugin, as you would not need to serve static resources from a cookies-free domain.
Removing cookies from static resources is not always the performance saver that some people think. This is totally not true in many cases.
In most cases the cookies aren't the cause of bad peformance, but the resources itselves. In those cases, it would be more effective totally removing the resources that you don't need everywhere with <a href="https://wordpress.org/plugins/freesoul-deactivate-plugins/">Freesoul Deactivate Plugins</a>.

Of course, removing cookies from static resources improves also the privacy of your visitors.

As a side note, removing cookies form static resources with this plugin will have no impact on the score given by some speed meters.
The speed meters only check if the static resources are requested to free-cookies domains, but they don't check the crossorigin paramenter.


== <a href="https://josemortellaro.com/remove-cookies-from-static-resources/">How to remove cookies from static resources</a> ==
* Install Remove Cookies From Static Resources
* Done!

== How to understand if I really need to remove cookies from static resources ==
* Go to your website
* Right-click => Ispect => Console => write document.cookie.length and press enter
* If you see a number higher than 5000 you probably need this plugin to save bandwidth due to big data transfers through the cookies. For lower numbers you will probably not need this plugin.

== Does removing cookies from static resources always improve the performance? ==
Absolutely not! It improves the performance only if yor website requests many HTTP requests due to static resources and it writes many data to the browser through the cookies.


== Limits ==
* This plugin doesn't work for old browsers that don't support the crossorigin attribute
* This plugin doesn't work for all those resources that are added with JavaScript or CSS, and probably it will never work in those cases, neither with future versions of the plugin.

== You may also be interested in ==
* <a href="https://wordpress.org/plugins/all-pages-in-customize/" target="_blank">All Pages In Customize</a>
* <a href="https://wordpress.org/plugins/asset-preloader/" target="_blank">Asset Preloader</a>
* <a href="https://wordpress.org/plugins/basic-security/" target="_blank">Basic Security</a>
* <a href="https://wordpress.org/plugins/blog-page-editor-for-elementor/" target="_blank">Blog Page Editor For Elementor</a>
* <a href="https://wordpress.org/plugins/body-class-by-url-parameter/" target="_blank">Body Class By Url Parameter</a>
* <a href="https://wordpress.org/plugins/change-class-in-viewport/" target="_blank">Change Class In Viewport</a>
* <a href="https://wordpress.org/plugins/change-debug-log-location/" target="_blank">Change Debug Log Location</a>
* <a href="https://wordpress.org/plugins/collect-browser-info/" target="_blank">Collect Browser Info</a>
* <a href="https://wordpress.org/plugins/content-no-cache/" target="_blank">Content No Cache</a>
* <a href="https://wordpress.org/plugins/css-selectors/" target="_blank">Css Selectors</a>
* <a href="https://wordpress.org/plugins/custom-spinner-for-woocommerce/" target="_blank">Custom Spinner For Woocommerce</a>
* <a href="https://wordpress.org/plugins/defer-transictional-emails-for-woocommerce/" target="_blank">Defer Transictional Emails For Woocommerce</a>
* <a href="https://wordpress.org/plugins/direct-password-reset-link/" target="_blank">Direct Password Reset Link</a>
* <a href="https://wordpress.org/plugins/disable-fatal-error-handler/" target="_blank">Disable Fatal Error Handler</a>
* <a href="https://wordpress.org/plugins/disable-global-style/" target="_blank">Disable Global Style</a>
* <a href="https://wordpress.org/plugins/editor-cleanup-for-avada/" target="_blank">Editor Cleanup For Avada</a>
* <a href="https://wordpress.org/plugins/editor-cleanup-for-divi-builder/" target="_blank">Editor Cleanup For Divi Builder</a>
* <a href="https://wordpress.org/plugins/editor-cleanup-for-elementor/" target="_blank">Editor Cleanup For Elementor</a>
* <a href="https://wordpress.org/plugins/editor-cleanup-for-flatsome/" target="_blank">Editor Cleanup For Flatsome</a>
* <a href="https://wordpress.org/plugins/editor-cleanup-for-oxygen/" target="_blank">Editor Cleanup For Oxygen</a>
* <a href="https://wordpress.org/plugins/editor-cleanup-for-wpbakery/" target="_blank">Editor Cleanup For Wpbakery</a>
* <a href="https://wordpress.org/plugins/email-no-bot/" target="_blank">Email No Bot</a>
* <a href="https://wordpress.org/plugins/essential-form/" target="_blank">Essential Form</a>
* <a href="https://wordpress.org/plugins/export-without-shortcodes/" target="_blank">Export Without Shortcodes</a>
* <a href="https://wordpress.org/plugins/freesoul-deactivate-plugins/" target="_blank">Freesoul Deactivate Plugins</a>
* <a href="https://wordpress.org/plugins/freesoul-responsive-check/" target="_blank">Freesoul Responsive Check</a>
* <a href="https://wordpress.org/plugins/freesoul-switch-theme/" target="_blank">Freesoul Switch Theme</a>
* <a href="https://wordpress.org/plugins/freeze/" target="_blank">Freeze</a>
* <a href="https://wordpress.org/plugins/frontend-as-any-user/" target="_blank">Frontend As Any User</a>
* <a href="https://wordpress.org/plugins/frontype/" target="_blank">Frontype</a>
* <a href="https://wordpress.org/plugins/hide-link/" target="_blank">Hide Link</a>
* <a href="https://wordpress.org/plugins/inline-image-base64/" target="_blank">Inline Image Base64</a>
* <a href="https://wordpress.org/plugins/lazy-load-control-for-elementor/" target="_blank">Lazy Load Control For Elementor</a>
* <a href="https://wordpress.org/plugins/load-video-on-click/" target="_blank">Load Video On Click</a>
* <a href="https://wordpress.org/plugins/mu-manager/" target="_blank">Mu Manager</a>
* <a href="https://wordpress.org/plugins/no-spam-in-backend/" target="_blank">No Spam In Backend</a>
* <a href="https://wordpress.org/plugins/oracle-cards/" target="_blank">Oracle Cards</a>
* <a href="https://wordpress.org/plugins/page-detector/" target="_blank">Page Detector</a>
* <a href="https://wordpress.org/plugins/passe-partout/" target="_blank">Passe Partout</a>
* <a href="https://wordpress.org/plugins/plugversions/" target="_blank">Plugversions</a>
* <a href="https://wordpress.org/plugins/progress-bar-correction-for-lifterlms/" target="_blank">Progress Bar Correction For Lifterlms</a>
* <a href="https://wordpress.org/plugins/rename-plugins-folder/" target="_blank">Rename Plugins Folder</a>
* <a href="https://wordpress.org/plugins/resource-not-found-placeholder/" target="_blank">Resource Not Found Placeholder</a>
* <a href="https://wordpress.org/plugins/restore-paypal-standard-for-woocommerce/" target="_blank">Restore Paypal Standard For Woocommerce</a>
* <a href="https://wordpress.org/plugins/save-single-file/" target="_blank">Save Single File</a>
* <a href="https://wordpress.org/plugins/specific-content-for-mobile/" target="_blank">Specific Content For Mobile</a>
* <a href="https://wordpress.org/plugins/top-bar-links/" target="_blank">Top Bar Links</a>
* <a href="https://wordpress.org/plugins/update-page-cache/" target="_blank">Update Page Cache</a>
* <a href="https://wordpress.org/plugins/website-information/" target="_blank">Website Information</a>


== Changelog ==

= 0.0.1 =
*Initial release
