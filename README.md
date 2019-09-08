
# Additional undesired hosts
This is a list of categorized domains, that are **guaranteed** not to break useful services.  Each domain is only added after through research and tests in order to make sure it should _intentionally be blocked_.

I intend to focus on _both_ web and mobile domains.

### Format
This list is available in **domains-only** format, with additional entries for wildcard blocking. You can use it with:
- [**Pi-hole**](https://pi-hole.net/) and/or [**DNScrypt-proxy**](https://simplednscrypt.org/).
- aggregated lists such as:
   - **1Hosts (Pro):** https://1hos.cf/Pro

I use [this](https://github.com/zeffy/dnscrypt-blocking-additions/blob/master/script/make_blacklist.py) python script alongside DNScrypt on my VPS instead of running Pi-hole.

### Blacklist Domains
| name                                    | description                                                   | domains format | hosts (IPv4) format |
| :-------------------------------------- | ------------------------------------------------------------- | :------------- | :------------------ |
| **adservers-and-trackers.txt**          | Blocks ads and trackers, and anything inbetween.              | [📝 `adservers-and-trackers.txt`](https://raw.githubusercontent.com/DRSDavidSoft/additional-hosts/master/domains/blacklist/adservers-and-trackers.txt) | _n/a_ |
| **activation.txt**                      | Blocks license verification and software activation.<br/><sup>This list is intended to prevent products from expiring when they detect an invalid license.</sup> | [📝 `activation.txt`](https://raw.githubusercontent.com/DRSDavidSoft/additional-hosts/master/domains/blacklist/activation.txt) | _n/a_ |
| **unwanted-iranian.txt**                | Blocks various scams and popups when visiting Iranian websites.<br/><sup>e.g. fake Download buttons, Pop-unders, etc</sup> | [📝 `unwanted-iranian.txt`](https://raw.githubusercontent.com/DRSDavidSoft/additional-hosts/master/domains/blacklist/unwanted-iranian.txt) | _n/a_ |

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
This repository is licensed under MIT License © 2019 David Refoua.  All re-distribution of my lists, provided that you credit my name and work, are encouraged and highly welcome.
