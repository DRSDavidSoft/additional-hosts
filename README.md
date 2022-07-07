
# Additional Undesired Hosts

[![License](https://img.shields.io/github/license/DRSDavidSoft/additional-hosts?style=flat-square)](https://github.com/DRSDavidSoft/additional-hosts/blob/master/LICENSE)
[![GitHub last commit](https://img.shields.io/github/last-commit/DRSDavidSoft/additional-hosts.svg?style=flat-square)](https://github.com/DRSDavidSoft/additional-hosts/commits/master)
[![GitHub commit activity the past year](https://img.shields.io/github/commit-activity/y/DRSDavidSoft/additional-hosts?style=flat-square)](https://github.com/DRSDavidSoft/additional-hosts/graphs/commit-activity)
[![Github file size](https://img.shields.io/github/repo-size/DRSDavidSoft/additional-hosts?label=total+size&style=flat-square)](github.com/DRSDavidSoft/additional-hosts/hosts/blob/master/hosts)

## Introduction
This is a list of categorized domains, with additional entries for wildcard blocking.  The domains are documented as to keep a record of what is being blocked or allowed.  The primary focus is to maximize blocking unwanted hosts while **guaranteeing** not to break any useful services or legitimate websites.  

Each domain is only added after through research and tests in order to make sure it should be _intentionally blocked_.  If you found _any_ domains that shouldn't be on these lists, please feel free to [open an issue](https://github.com/DRSDavidSoft/additional-hosts/issues/new).

Thanks for reporting issues, and using my lists! ❤️

## Blacklist Domains
| List Title                              | Description                                                   | Download List         |
| --------------------------------------- | ------------------------------------------------------------- | --------------------- |
| **Ad and tracker servers**              | Blocks advertisement and trackers, and anything inbetween.<br/><sup>Pop Ups, Pop Unders, Gif Banners, Game Ads, Ads CDNs, etc.</sup>    | [📝 `adservers-and-trackers.txt`](https://raw.githubusercontent.com/DRSDavidSoft/additional-hosts/master/domains/blacklist/adservers-and-trackers.txt) |
| **Activation servers**                  | Blocks license verification and software activation.<br/><sup>This list is intended to prevent products from expiring when they detect an invalid license.</sup> | [📝 `activation.txt`](https://raw.githubusercontent.com/DRSDavidSoft/additional-hosts/master/domains/blacklist/activation.txt) |
| **Fake domains**                        | Blocks copycat, scam and fake domains.</br><sup>These domains may imitate other well-known websites for various reasons, or promise to provide a functionality that they actually don't do.</sup> | [📝 `fake-domains.txt`](https://raw.githubusercontent.com/DRSDavidSoft/additional-hosts/master/domains/blacklist/fake-domains.txt) |
| **Search blacklist**                    | Blocks useless, shady and annoying domains from from appearing in search engine results. | [📝 `search-blacklist.txt`](https://raw.githubusercontent.com/DRSDavidSoft/additional-hosts/master/domains/blacklist/search-blacklist.txt) |
| **Unwanted Iranian domains**            | Blocks various regional scams and popups specific to Iranian websites.<br/><sup>e.g. Pop Ups, Fake Download Buttons, Scam Landing Pages, Trackers, etc.</sup> | [📝 `unwanted-iranian.txt`](https://raw.githubusercontent.com/DRSDavidSoft/additional-hosts/master/domains/blacklist/unwanted-iranian.txt) |

_It is recommended that these lists be used in CNAME, Wildcard blocking mode._

**👉 NOTE:** Additional wildcard domains are present in the [📁 `/wildcard-domains/blacklist`](https://github.com/DRSDavidSoft/additional-hosts/tree/master/wildcard-domains/blacklist) directory.

## Whitelist Domains
The `whitelist` domains that I use – which are also hand-picked – are being categorized, and _will_ be published under the [📁 `/domains/whitelist`](https://github.com/DRSDavidSoft/additional-hosts/blob/master/domains/whitelist) directory when released.  
In the meantime, please contact me if you'd like to receive information about my whitelists.

## Format
The lists are provided only in **domains** format at the moment, with the following properties:

- The `#` or `!` denotes a **comment**, and may come at at the beginning of a line, or after an entry.
- Lines only contain a single hostname.
- The `*` character represents a wild-card (which [**Pi-hole**](https://pi-hole.net/) might _not_ support, but [**DNSCrypt-proxy**](https://dnscrypt.info/) will – which is what I'm using at the moment.)
- All whitespace (including new line, tabs, spaces, etc) should be ignored.

Other lists can feel free to remove all whitespace and comments from my lists when/if mine are included.

**👉 NOTE:** If you would like to use my lists as your `/etc/hosts` file, first you would need to convert the domains format to `IPv4` (i.e. `127.0.0.1` or `0.0.0.0`) format.  However, since the hosts file does not support wildcard and/or CNAME blocking, I haven't provided this format for download.  A conversion is needed (adding the required `0.0.0.0` prefix), before it can be used as a HOSTS file.

## Sources
The domain entries on this list are hand-picked, and mainly added by analyzing the traffic generated by the devices I use.  I intend to focus on domains related to _both_ websites and mobile apps.  This will include the obvious pop-ups and pop-unders, frame-based ads, 3<sup>rd</sup> party image and video ads, mobile in-app banners -- as well as hidden tracking and other unnecessary bloated spyware that is ususally bundled with common apps that are downloaded, and the websites you visit.

## Software
The provided lists are compatible with:  
- [**<img height=32 align=middle src="https://pi-hole.github.io/graphics/Vortex/Vortex_with_Wordmark.svg"> Pi-hole**](https://pi-hole.net/) and/or [**<img height=32 align=middle src="https://raw.githubusercontent.com/DNSCrypt/dnscrypt-proxy/master/logo.png"> DNScrypt-proxy**](https://simplednscrypt.org/).
- [**<img height=24 align=middle src="http://www.squid-cache.org/favicon.ico"> Squid**](http://www.squid-cache.org/) proxy ([Windows downloads](http://squid.diladele.com/), [How-to use](http://www.thedumbterminal.co.uk/posts/2005/10/blocking_access_to_sites_when_using_squid.html))
- [**<img height=24 align=middle src="https://raw.githubusercontent.com/gorhill/uBlock/master/doc/img/icon38@2x.png"> uBlock Origin**](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm?hl=en) and/or [**<img width=24 align=middle src="https://adblockplus.org/favicon.ico"> Adblock Plus**](https://adblockplus.org/download)
- [**<img height=24 align=middle src="https://adguard.com/img/favicons/favicon.ico"> AdGuardHome**](https://github.com/AdguardTeam/AdGuardHome#getting-started)

You can use it on either a server, or using browser extensions, you can filter sites on the client side.

🕳 Read **[Olivier Butterbach](https://github.com/obutterbach)**'s excellent post on Medium to set up Pi-hole:  
https://medium.com/@obutterbach/unlock-the-full-potential-of-pihole-e795342e0e36

## Aggregated lists
The following aggregated lists automatically includes the domains in my lists.  You can use the aggregated lists such as:
- **[1Hosts (Pro)](https://github.com/badmojr/1Hosts/tree/master/Pro)** – includes `adservers-and-trackers` and `unwanted-iranian` lists
- **[oisd.nl](https://oisd.nl/?p=dl)** – includes `adservers-and-trackers` and `unwanted-iranian` lists

I used to use [this](https://github.com/zeffy/dnscrypt-lists/blob/9d776690e901e106ea5707e4c83f73a07ed2470d/script/make_blacklist.py) python script alongside DNScrypt on my VPS instead of running Pi-hole.

**✍ Note:**  You're welcome to use and include my lists in your aggregated lists and redistribute them.  Please [tell me](https://github.com/DRSDavidSoft/additional-hosts/issues/new?title=Mention+my+list) if you do so, so I can mention your list here as well.

## Sources to use alongside mine
These are some of the other lists that you should _definitely_ be using alongside with mine:  

- [Peter Lowe’s Ad and tracking server list](https://pgl.yoyo.org/adservers/):  
    `https://pgl.yoyo.org/adservers/serverlist.php?hostformat=hosts&showintro=1&mimetype=plaintext`
- [Dan Pollock’s hosts file](https://someonewhocares.org/hosts/):  
    `https://someonewhocares.org/hosts/hosts`
- [MVPS HOSTS file](https://winhelp2002.mvps.org/hosts.htm):  
    `https://winhelp2002.mvps.org/hosts.txt`
- [Steven Black's host file](https://github.com/StevenBlack/hosts):  
    `https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts`
- [Lightswitch05's Ads and tracking hosts](https://github.com/lightswitch05/hosts):  
    `https://www.github.developerdan.com/hosts/lists/ads-and-tracking-extended.txt`
- [AdAway Hosts](https://github.com/AdAway/AdAway/wiki/HostsSources):  
    `https://adaway.org/hosts.txt`
- [AdguardDNS](https://adguard-dns.io/en/welcome.html):  
    `https://v.firebog.net/hosts/AdguardDNS.txt`
- [WaLLy3K's Ads and trackers personal blacklist](https://firebog.net/about):  
    `https://v.firebog.net/hosts/static/w3kbl.txt`
- [anudeepND's Blacklist](https://github.com/anudeepND/blacklist):  
    `https://raw.githubusercontent.com/anudeepND/blacklist/master/adservers.txt`
- [EasyList and EasyPrivacy](https://github.com/easylist/easylist):
    - `https://v.firebog.net/hosts/Easylist.txt`
    - `https://justdomains.github.io/blocklists/lists/easyprivacy-justdomains.txt`

## Set-Up / Configuration
I combine my lists with some other lists and generate a final `domains-blacklist.txt` file, that is used on the two servers that I run (one as a redundant).  
<sub>The source list includes ~1500 links, and resolves to about 80 million records (14 million unique top-level domains).  The servers both have **8GBs** of RAM, and for my usecase about ~15% CPU load on average.</sub>

_P.S._ Personally I haven't ran into any major issues blocking this many domains, altough some people consider blocking any amount over >1M domains to be overkill.

**Here's a diagram of software setup on both of the servers:**

```
                    ╭────────────────╮   ╭──────────────────╮
╔═════════════╗     │                │   │                  │
║  DoH / DoT  ║     │                │   │                  │ UDP Tunnel    ┌─────────┐
║             ║  →  │ DNSCrypt-Proxy │ → │ Unbound resolver │ … … … … … … → │ Clients │
║  Providers  ║     │                │   │                  │               └─────────┘
╚═════════════╝     │                │   │                  │
                    ╰────────────────╯   ╰──────────────────╯
```

The clients can connect over a secure UDP tunnel (e.g. either on Desktop or mobile).

## Report domains
If you notice any domains that you believe should be included in my lists, please report it to me [here](issues/new).  

A great deal of care is taken to avoid any type of false positives.  However, in the event that you see something legitamate is being blocked, missing content and/or breaking functionality, please report false positives by creating an issue [here](issues/new).

This could be because the domain names that serve those type of ads could potentially be also used to serve legitimate content, which means blocking them will result in an app or website missing content or losing functionality.

These lists are personaly used by me, with no side-effects.  I have kept the lists short and lightweight, while adding as much as possible to each list.

## Updates
In order to get notified of an update, you can mark my repository as "watched".  I update this list on a weekly or monthly basis.

**Subscribe to FilterLists entries**:
- https://filterlists.com/lists/additional-hosts-adservers-and-trackers
- https://filterlists.com/lists/additional-hosts-unwanted-iranian

## License
This repository is licensed under MIT License © 2019-2020 David Refoua.  All re-distribution of my lists, provided that you credit my name and work, are welcome and encouraged.
