
# Additional Undesired Hosts

[![License](https://img.shields.io/github/license/DRSDavidSoft/additional-hosts?style=flat-square)](https://github.com/DRSDavidSoft/additional-hosts/blob/master/LICENSE)
[![GitHub last commit](https://img.shields.io/github/last-commit/DRSDavidSoft/additional-hosts.svg?style=flat-square)](https://github.com/DRSDavidSoft/additional-hosts/commits/master)
[![GitHub commit activity the past year](https://img.shields.io/github/commit-activity/y/DRSDavidSoft/additional-hosts?style=flat-square)](https://github.com/DRSDavidSoft/additional-hosts/graphs/commit-activity)
[![Github file size](https://img.shields.io/github/repo-size/DRSDavidSoft/additional-hosts?label=total+size&style=flat-square)](github.com/DRSDavidSoft/additional-hosts/hosts/blob/master/hosts)

This is a list of categorized domains, with additional entries for wildcard blocking.  The primary focus is to **guarantee** not to break any useful services or legitimate websites.  Each domain is only added after through research and tests in order to make sure it should _intentionally be blocked_.

I intend to focus on _both_ websites and mobile domains.

### Format
This list is available in **domains-only** format at the moment, which is compatible with:
- [**<img width=24 align=middle src="https://piholenet.b-cdn.net/wp-content/uploads/2016/12/cropped-Vortex-3.png"> Pi-hole**](https://pi-hole.net/) and/or [**<img width=24 align=middle src="https://dnscrypt.info/_nuxt/img/dnscrypt.cd47d19.png"> DNScrypt-proxy**](https://simplednscrypt.org/).
- [**<img width=24 align=middle src="http://www.squid-cache.org/favicon.ico"> Squid**](http://www.squid-cache.org/) proxy ([Windows downloads](http://squid.diladele.com/), [How-to use](http://www.thedumbterminal.co.uk/posts/2005/10/blocking_access_to_sites_when_using_squid.html))
- [**<img width=24 align=middle src="https://raw.githubusercontent.com/gorhill/uBlock/master/doc/img/icon38@2x.png"> uBlock Origin**](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm?hl=en) and/or [**<img width=24 align=middle src="https://adblockplus.org/favicon.ico"> Adblock Plus**](https://adblockplus.org/download)

You can use it on either a server, or within browser plugins, so you can filter sites on the client side.

### Aggregated lists
The following aggregated lists automatically includes the domains in my lists.  You can use the aggregated lists such as:
- **1Hosts (Pro):** https://1hos.cf/Pro

I use [this](https://github.com/zeffy/dnscrypt-blocking-additions/blob/master/script/make_blacklist.py) python script alongside DNScrypt on my VPS instead of running Pi-hole.

### Blacklist Domains
| name                                    | description                                                   | domains format | hosts (IPv4) format |
| :-------------------------------------- | ------------------------------------------------------------- | :------------- | :------------------ |
| **Ad and tracker servers**              | Blocks ads and trackers, and anything inbetween.              | [📝 `adservers-and-trackers.txt`](https://raw.githubusercontent.com/DRSDavidSoft/additional-hosts/master/domains/blacklist/adservers-and-trackers.txt) | _n/a_ |
| **Activation servers**                  | Blocks license verification and software activation.<br/><sup>This list is intended to prevent products from expiring when they detect an invalid license.</sup> | [📝 `activation.txt`](https://raw.githubusercontent.com/DRSDavidSoft/additional-hosts/master/domains/blacklist/activation.txt) | _n/a_ |
| **Unwanted Iranian domains**            | Blocks various scams and popups when visiting Iranian websites.<br/><sup>e.g. fake Download buttons, Pop-unders, etc</sup> | [📝 `unwanted-iranian.txt`](https://raw.githubusercontent.com/DRSDavidSoft/additional-hosts/master/domains/blacklist/unwanted-iranian.txt) | _n/a_ |

### Whitelist Domains
_TBA:_ to be added

### Sources to use alongside mine
_TBA:_ to be added

### Report domains
If you notice any domains that you believe should be included in my lists, please report it to me [here](issues/new).  

### Note
A great deal of care is taken to avoid any type of false positives.  However, in the event that you see something legitamate is being blocked, missing content and/or breaking functionality, please report false positives by creating an issue [here](issues/new).

This could be because the domain names that serve those type of ads could potentially be also used to serve legitimate content, which means blocking them will result in an app or website missing content or losing functionality.

### Updates
In order to get notified of an update, you can mark my repository as "watched". I update this list on a weekly basis.

### License
This repository is licensed under MIT License © 2019 David Refoua.  All re-distribution of my lists, provided that you credit my name and work, are welcome and encouraged.
