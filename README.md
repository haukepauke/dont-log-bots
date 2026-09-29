Don't Log Bots [![Listed in Awesome YOURLS!](https://img.shields.io/badge/Awesome-YOURLS-C5A3BE)](https://github.com/YOURLS/awesome-yourls/)
=============

Plugin for [YOURLS](https://yourls.org) `1.10.*`, running on PHP `8.5`.

Description
-----------
Ignore bot hits in your stats (both click count as seen in the main admin page and in detailed stats).

Installation
------------
1. In `/user/plugins`, create a new folder named `dont-log-bots`.
2. Drop these files in that directory.
3. Go to the Plugins administration page ( *eg* `http://sho.rt/admin/plugins.php` ) and activate the plugin.
4. Have fun!

License
-------
YOURLS' license, aka *"Do whatever the hell you want with it"*. 
_YOURLS - MIT License_

More
----

The list includes search crawlers, AI crawlers, and social-preview bots. It is based on user agents observed in YOURLS installations and public crawler identifiers. There is no reliable way to determine whether a client is a bot, and user agents can be spoofed.

To check user agents on your own setup, you can try this query:

```mysql
SELECT DISTINCT `user_agent` as ua, COUNT(*) as c FROM `yourls_log` GROUP BY ua ORDER BY c DESC
```
