=== Reverse-Proxy Comment IP Fix ===
Contributors: gnotaras
Tags: 
Requires at least: 1.5.2
Tested up to: 4.5
Stable tag: 0.2.0
License: Apache License v2
License URI: http://www.apache.org/licenses/LICENSE-2.0.txt

Sets the comment IP to the client IP provided by the X-Forwarded-For or X-Real-IP headers. [DEPRECATED]


== Description ==

Sets the comment IP to the client IP provided by the X-Forwarded-For or X-Real-IP headers before the comment is saved to the database.

Note: Please note that the existence of trustworthy information in the `X-Forwarded-For` and the `X-Real-IP` HTTP headers is up to the system administrator. HTTP clients can send HTTP headers containing invalid information. It is highly recommended to reset these headers at the first web proxy server you trust.

**NOTICE:** THIS PLUGIN HAS BEEN **DEPRECATED**. IT IS NO LONGER SUPPORTED. IT IS NO LONGER TESTED WITH NEW WORDPRESS RELEASES. USING IT IN PRODUCTION IS NOT RECOMMENDED.

IT IS STRONGLY SUGGESTED TO MIGRATE TO OTHER MORE MODERN AND BETTER MAINTAINED PLUGINS.

IF YOU ARE STARTING A NEW BLOG, IT IS HIGHLY RECOMMENDED TO SEARCH FOR OTHER PLUGINS IN ORDER TO AVOID THE INEVITABLE FUTURE MIGRATION.

REGARDING EXISTING USERS, AT THE TIME OF WRITING, THERE ARE NO MAJOR BUGS. PROVIDED THAT THE WORDPRESS API DOES NOT CHANGE SOON, YOU HAVE THE TIME TO EXPERIMENT WITH OTHER PLUGINS AND PLAN YOUR MIGRATION.

<blockquote>

<strong>Important Notice</strong>

<br /><br />

I have stopped using this plugin and therefore I won't be supporting it or testing it with any new WordPress releases in the future. I highly recommend switching to a mechanism that is specific to your web server in order to do what this plugin does. Please check your web server's documentation or community support forums for more information. Please note that by continuing using this plugin you are on your own.

<br /><br />

</blockquote>

= Official Project Homepage =

The Reverse-Proxy Comment IP Fix project information and documentation has been moved to the [Reverse-Proxy Comment IP Fix Development Web Site](http://www.codetrax.org/projects/reverse-proxy-comment-ip-fix/wiki).


== Installation ==

1. Extract the compressed (zip) package in the `/wp-content/plugins/` directory.
2. Activate the plugin through the 'Plugins' menu in WordPress

== Frequently Asked Questions ==

= Does this plugin just work? =

Yes. After activation, there are no more configuration steps.

= How can the plugin determine that the client IP address contained in the `X-Forwarded-For` and the `X-Real-IP` HTTP headers is the real one? =

It can't. There is no way that the plugin can make any decision about whether the information contained in the `X-Forwarded-For` and the `X-Real-IP` HTTP headers is real or not. This decision has to be taken by the system administrator. The general idea is that the first trusted web proxy should be configured in such a way so that these headers are reset at that point and thereafter contain only information the system administrator trusts.

= Are there any alternative ways to set the client's real IP address in the REMOTE_ADDR server variable? =

Although this question is outside the scope of this FAQ, indeed, this can be done. If your web server is *Apache*, you can use one the following modules: [mod_remoteip](http://httpd.apache.org/docs/2.4/mod/mod_remoteip.html) (httpd >= 2.4), [mod_rpaf](https://github.com/gnif/mod_rpaf), [mod_extract_forwarded](http://www.openinfo.co.uk/apache/). In case you use *Nginx*, check the [ngx_http_realip_module](http://nginx.org/en/docs/http/ngx_http_realip_module.html).

All these modules can extract the client's IP address from user-defined HTTP headers and update the `REMOTE_ADDR` server variable. In that case, this plugin is no longer needed in your WordPress installation, as the real IP address of the client is directly available in the server variables.

= Do you use this plugin? =

This plugin has been deprecated.


== Changelog ==

**NOTICE:** THIS PLUGIN HAS BEEN **DEPRECATED**. IT IS NO LONGER SUPPORTED. IT IS NO LONGER TESTED WITH NEW WORDPRESS RELEASES. USING IT IN PRODUCTION IS NOT RECOMMENDED.

IT IS STRONGLY SUGGESTED TO MIGRATE TO OTHER MORE MODERN AND BETTER MAINTAINED PLUGINS.

IF YOU ARE STARTING A NEW BLOG, IT IS HIGHLY RECOMMENDED TO SEARCH FOR OTHER PLUGINS IN ORDER TO AVOID THE INEVITABLE FUTURE MIGRATION.

REGARDING EXISTING USERS, AT THE TIME OF WRITING, THERE ARE NO MAJOR BUGS. PROVIDED THAT THE WORDPRESS API DOES NOT CHANGE SOON, YOU HAVE THE TIME TO EXPERIMENT WITH OTHER PLUGINS AND PLAN YOUR MIGRATION.

Please read the dynamic [changelog](http://www.codetrax.org/projects/reverse-proxy-comment-ip-fix/roadmap "Reverse-Proxy Comment IP Fix ChangeLog")

- [0.2.0](http://www.codetrax.org/versions/358)
 - Major refactoring.
 - IP validation supporting both IPv4 and IPv6.
 - Support for the X-Real-IP header in addition to the X-Forwarded-For.
- [0.1.1](http://www.codetrax.org/versions/219)
 - Updated plugin metadata for compatibility with WordPress 3.8.X
- [0.1.0](http://www.codetrax.org/versions/124)
 - Initial release
