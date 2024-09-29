[![GitHub issues](https://img.shields.io/github/issues/yokoffing/NextDNS-Config)](https://github.com/yokoffing/NextDNS-Config/issues)
![GitHub](https://img.shields.io/github/license/yokoffing/NextDNS-Config?color=blue)
![GitHub Maintained](https://img.shields.io/badge/Open%20Source-Yes-green)
![GitHub commit activity](https://img.shields.io/github/commit-activity/y/yokoffing/NextDNS-Config)
![GitHub last commit](https://img.shields.io/github/last-commit/yokoffing/NextDNS-Config)
![GitHub Maintained](https://img.shields.io/badge/maintained-yes-green)
[![Hits]()](https://hits.seeyoufarm.com)

***
# Guidelines :bookmark:
1) Prevent overblocking by utilizing the [law of diminishing returns]() (e.g., using [sane](https://www.privacyguides.org/en/basics/threat-modeling/), quality [blocklists](https://github.com/yokoffing/NextDNS-Config#blocklists-1); allowing most [TLDs](https://github.com/yokoffing/NextDNS-Config#block-top-level-domains-tlds-1-2-3-4-5-); etc.).
2) Pass the [girlfriend test](https://www.urbandictionary.com/define.php?term=Grandma%20Test) with few exceptions. These deviations are documented throughout the guide.

***

## Create your account

Sign up for NextDNS [here](https://nextdns.io/?from=xujj63g5) and support this page!

***

# Security :police_officer:

Security settings protect your data from harm, theft, and unauthorized use.<sup>*^[why does this matter?](https://thenewoil.org/en/guides/prologue/why)*</sup>

## Threat Intelligence Feeds <sup><sup>[1](https://github.com/nextdns/metadata/blob/6f9b6cd0670e7e31ad2ca716742088c2fc0616c2/security/threat-intelligence-feeds.json)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Use Threat Intelligence Feeds
## AI-Driven Threat Detection <sup><sup>[1](https://x.com/NextDNS/status/1440291577713233925)</sup></sup>
> [!NOTE]
> NextDNS labels this feature as [beta](https://www.vocabulary.com/dictionary/beta), although most users report it works well.

![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable AI-Driven Threat Detection

## Google Safe Browsing <sup><sup> [1](https://safebrowsing.google.com/safebrowsing/report_general/) [2](https://blog.cryptographyengineering.com/2019/10/13/dear-apple-safe-browsing-might-not-be-that-safe/) [3](https://the8-bit.com/apple-proxies-google-safe-browsing-privacy/) [4](https://github.com/brave/brave-browser/wiki/Deviations-from-Chromium-(features-we-disable-or-remove)#services-we-proxy-through-brave-servers) </sup></sup>
> [!TIP]
> Unlike the version embedded in some browsers, this feature does not associate your public IP address to threats and does not allow bypassing the block. 

![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable Google Safe Browsing

## Cryptojacking Protection <sup><sup>[1](https://github.com/nextdns/metadata/blob/6f9b6cd0670e7e31ad2ca716742088c2fc0616c2/security/cryptojacking.json)</sup></sup>
> [!CAUTION]
> Leave this feature enabled if you use something other than the [recommended blocklists](https://github.com/yokoffing/NextDNS-Config#privacy-lock) (see https://github.com/yokoffing/NextDNS-Config/issues/31).

![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Enable Cryptojacking Protection

## DNS Rebinding Protection <sup><sup>[1](https://help.nextdns.io/t/35hmval/what-is-dns-rebinding-protection) [2](https://www.reddit.com/r/nextdns/comments/t0ne8r/does_dns_rebinding_protection_block_remote_access/?context=3)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg)  Enable DNS Rebinding Protection
## IDN Homograph Attacks Protection <sup><sup>[1](https://web.archive.org/web/20230325073817/https://blog.riotsecurityteam.com/idn-homograph-attacksprevention) [2](https://akamai.com/blog/security/watch-your-step-the-prevalence-of-idn-homograph-attacks)</sup></sup>
![Enabled]() Enable Homograph Attacks Protection
## Typosquatting Protection <sup><sup>[1](https://github.com/nextdns/metadata/blob/6f9b6cd0670e7e31ad2ca716742088c2fc0616c2/security/typosquatting/protected-domains)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable Typosquatting Protection
## Domain Generation Algorithms (DGAs) Protection
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable DGA Protection
## Block Newly Registered Domains (NRDs) <sup><sup>[1](https://boldgrid.com/instagram-influencer-accounts-are-being-hacked-phishing-attacks) </sup></sup>
> [!WARNING]
> Blocking NRDs may cause [false positives](https://csrc.nist.gov/glossary/term/false_positive) [occasionally](https://www.reddit.com/r/InternetIsBeautiful/comments/w2wdro/comment/iguvg8y/?context=3). Be selective when adding NRDs to your allowlist; and, if you do, **NEVER** give [sensitive information](https://egnyte.com/guides/governance/sensitive-information) to a NRD. *If you plan to [set-and-forget](https://glosbe.com/en/en/set-and-forget) your configuration, disable this setting.*

![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Block Newly Registered Domains (NRDs)

## Block Dynamic DNS Hostnames <sup><sup>[1](https://github.com/nextdns/ddns-domains/blob/main/suffixes) [2](https://x.com/NextDNS/status/1541740963760144386) </sup></sup>
> [!TIP]
> Dynamic DNS (DDNS) services can still access their own website and update API when you use this setting.

![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable Block Dynamic DNS Hostnames

## Block Parked Domains <sup><sup>[1](https://github.com/nextdns/metadata/blob/6f9b6cd0670e7e31ad2ca716742088c2fc0616c2/security/parked-domains-cname)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Block Parked Domains
## Block Top-Level Domains (TLDs) <sup><sup>[1](https://webtribunal.net/blog/tld-statistics/) [2](https://www.spamhaus.org/reputation-statistics/cctlds/domains/) [3](https://bleepingcomputer.com/news/security/verified-twitter-accounts-hacked-to-send-fake-suspension-notices/) [4](https://github.com/DandelionSprout/adfilt/blob/master/Dandelion%20Sprout's%20Anti-Malware%20List.txt) [5](https://github.com/DandelionSprout/adfilt/issues/659#issuecomment-1284845803) </sup></sup>
*Updated: 18 March 2024* <p>

> [!IMPORTANT]
> Blocking [TLDs](https://www.geeksforgeeks.org/components-of-a-url) risks blocking legitimate sites along with malicious ones, since this feature stops both site navigations and subrequests. However, the entries below should allow for everyday browsing while offering protection against commonly abused TLDs.

<details><summary>Click me to view TLDs</summary>

```
.autos
.best
.bid
.bio
.boats
.boston
.boutique
.charity
.christmas
.dance
.fishing
.hair
.haus
.loan
.loans
.men
.mom
.name
.review
.rip
.skin
.support
.tattoo
.tokyo
.voto
```

</details>

You can find additional entries on [Most Abused TLDs](https://github.com/hagezi/dns-blocklists?tab=readme-ov-file#tlds), but you may need to [allowlist](https://github.com/yokoffing/NextDNS-Config#allowlist-white_check_mark) sites on occasion. *If you plan to [set-and-forget](https://glosbe.com/en/en/set-and-forget) your configuration, skip this step.*

## Block Child Sexual Abuse Material
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Block Child Sexual Abuse Material

***

# Privacy :lock:
Privacy features limit the amount of data companies can collect about you.

Because privacy is a [spectrum](https://blog.thenewoil.org/the-privacy-myth-binary-vs-spectrum), what you need varies on your [threat model](https://thenewoil.org/en/guides/prologue/threat-model/), interest, and skillset.<sup>^[*why should I care? I have nothing to hide*](https://medium.com/@FabioAEsteves/i-have-nothing-to-hide-why-should-i-care-about-my-privacy-f488281b8f1d)</sup>

## Blocklists <sup><sup>[1](https://github.com/nextdns/blocklists/tree/main/blocklists)</sup></sup>

Blocklists filter out ads, [trackers](https://www.freecodecamp.org/news/what-you-should-know-about-web-tracking-and-how-it-affects-your-online-privacy-42935355525/), and malicious sites. Hundreds of volunteers contribute to these lists in the [open-source](https://opensource.com/resources/what-open-source) community, and they are the undercover heroes who make blocking ads at scale possible.

We recommend you **remove** the [NextDNS Ads & Trackers Blocklist](https://github.com/nextdns/blocklists/blob/main/blocklists/nextdns-recommended.json) and **add** the [minimum](https://www.reddit.com/r/nextdns/comments/1048xeg/do_you_use_nextdns_blocklist_as_the_primary/j33wnz2/?context=3) number of useful lists.

### Which blocklist should I use?

A great question to ask is: "How much do I want to deal with the inconveniences of [false positives](https://csrc.nist.gov/glossary/term/false_positive)?"

Here are the suggested blocklists, based on past issues and observations:

|     **Blocklists**   |                              **Rationale**                                             |
|:--------------------:|:--------------------------------------------------------------------------------------:|
| HaGeZi - <br>Multi **NORMAL**<sup>[1](https://github.com/hagezi/dns-blocklists/blob/main/statistics.md#multi)</sup> <p><p>OISD</p> | Block tracker, ad, and badware requests without issues ([set-and-forget](https://glosbe.com/en/en/set-and-forget)). |
| HaGeZi - <br>Multi **PRO**<sup>[2](https://github.com/hagezi/dns-blocklists/blob/main/statistics.md#pro)</sup> <p><p>OISD</p> | Block more requests, usually without issues (recommended). |
| HaGeZi - <br>Multi **PRO++**<sup>[3](https://github.com/hagezi/dns-blocklists/blob/main/statistics.md#proplus)</sup> <p><p>OISD</p> | Block more requests at the risk of site breakage. <br> [Report](https://github.com/hagezi/dns-blocklists/issues/new/choose) occasional site and app issues. |

> [!TIP]
> Use different blocklists on separate DNS profiles (e.g., NORMAL for your router and PRO++ for your web browser).

> [!NOTE]
>  NextDNS does not offer Hagezi's Threat Intelligence Feed (TIF). We suggest using the OISD list, which contains some TIF sources missing from NextDNS security features.

You can also check out Hagezi's own [recommendations](https://github.com/hagezi/dns-blocklists/tree/main#whatshouldiuse).

### Why Hagezi?
[Hagezi](https://github.com/hagezi/dns-blocklists) block ads, trackers, native device trackers, and badware. He maintains a sensible allowlist, handles false positives quickly, and communicates known issues to blocklists maintainers. Hagezi's primary DNS lists combine multiple [sources](https://github.com/hagezi/dns-blocklists/wiki/FAQ#-which-sources-are-used-for-the-lists-and-how-are-the-lists-compiled-on-the-basis-of-these-sources) including respected community blocklists like [OISD](https://oisd.nl/), [Steven Black](https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts), [1Hosts](https://github.com/badmojr/1Hosts#safeguard-your-devices-against-pesky-ads-trackers-and-malware), [notrack](https://gitlab.com/quidsup/notrack#notrack), and [more](https://github.com/hagezi/dns-blocklists/blob/main/sources.md).

You may also wonder why other lists are not utilized. This is because many list maintainers:
* do not remove [false positives](https://csrc.nist.gov/glossary/term/false_positive) and/or are no longer active <sup>[1](https://github.com/lightswitch05/hosts/issues/356) [2](https://github.com/EnergizedProtection/block/issues/916)</sup>
* already [aggregate](https://www.reddit.com/r/nextdns/comments/ys3s1s/confused_about_blocklists/ivxdcd2/?context=3) common blocklists into their own list (Easylist/Fanboy, AdGuard, Steven Black, etc.) <sup>[1](https://github.com/badmojr/1Hosts/blob/master/-data/lists/assets.txt) [2](https://oisd.nl/includedlists/big/0) [3](https://github.com/jerryn70/GoodbyeAds/blob/master/Docs/Sources.md) [4](https://github.com/hagezi/dns-blocklists/blob/main/sources.md#sources) </sup>
* offer no meaningful additional coverage when compared with the chart combinations above

## Native Tracking Protection <sup><sup>[1](https://github.com/nextdns/native-tracking-domains/tree/main/domains)</sup></sup>

Add all the device brands you use.

<details>

	Windows
	Apple
	Samsung
	Xiaomi
	Huawei
	Amazon Alexa
	Roku
	Sonos

</details>

## Block Disguised Third-Party Trackers <sup><sup>[1](https://github.com/nextdns/cname-cloaking-blocklist/blob/master/domains) [2](https://www.reddit.com/r/nextdns/comments/10nenu3/disguised_trackers_are_blocked_regardless_of) [3](https://medium.com/nextdns/cname-cloaking-the-dangerous-disguise-of-third-party-trackers-195205dc522a) [4](https://arxiv.org/pdf/2102.09301.pdf) [5](https://tma.ifip.org/2020/wp-content/uploads/sites/9/2020/06/tma2020-camera-paper66.pdf) </sup></sup>
![Enabled]() Block Disguised Third-Party Trackers

## Allow Affiliate & Tracking Links <sup><sup>[1](https://github.com/nextdns/click-tracking-domains) [2](https://x.com/NextDNS/status/1539229377560461312) </sup></sup>
> [!TIP]
> Your IP address will automatically be hidden (via [TCP](https://educba.com/what-is-tcp-ip) [proxying](https://en.wikipedia.org/wiki/Proxy_server#/media/File:Proxy_concept_en.svg)) to preserve your privacy.<p>

> [!WARNING]
> Disabling this setting prevents some email links from opening properly.

![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Allow Affiliate & Tracking Links

***

# Parental Control :family_man_woman_boy:
## YouTube Restricted Mode
![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Enforce YouTube Restricted Mode
## Block Bypass Methods <sup><sup>[1](https://github.com/nextdns/dns-bypass-methods)</sup></sup>
Block tools that can bypass NextDNS filtering, such as VPNs, proxies, Tor software, and encrypted DNS services.
> [!CAUTION]
> Enabling this setting causes unintended behavior.

![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Block Bypass Methods

***

# Denylist :no_entry:

Denylist entries are always blocked. These entries may further harden some profiles while not interfering with everyday browsing.

### iCloud Private Relay

[iCloud Private Relay](https://support.apple.com/en-us/102602) can override DNS settings on devices, preventing NextDNS from protecting them.

Some DoH providers block this feature automatically.

	mask.icloud.com
	mask-h2.icloud.com

And possibly:

  	apple-relay.cloudfare.com
    apple-relay.fastly-edge.com
	doh.dns.apple.com
	doh.dns.apple.com.v.aaplimg.com

***

# Allowlist :white_check_mark:

Allowlist entries always resolve. These entries may be needed for aggressive DNS profiles to relax their rules.

### NextDNS

Allow NextDNS itself in case a filterlist goes [haywire](https://help.nextdns.io/t/m1hs207/energized-ultimate-lists-blocking-nextdns) and blocks your access.

	nextdns.io

<details><summary>Click here to view more entries</summary>

### Facebook / Instagram <sup><sup>[1](https://github.com/jerryn70/GoodbyeAds/issues/309)</sup></sup> 

	graph.facebook.com
	graph.instagram.com
	i.instagram.com
	b-graph.facebook.com

If you're still having issues, try [these](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/share/facebook.txt):
	
	connect.facebook.com
	connect.facebook.net
	graph-fallback.facebook.com
	z-m-graph.facebook.com
	graph-fallback.instagram.com

### Apple device updates <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/536) [2](https://github.com/badmojr/1Hosts/issues/562) [3](https://github.com/nextdns/metadata/pull/1132#issuecomment-1331733770)

A [known tracking domain](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558), but it's needed for device updates.

	xp.apple.com

### Apple iMessage GIFs <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/560)</sup></sup> / Spotlight Search <sup><sup>[2](https://github.com/badmojr/1Hosts/issues/562)</sup></sup> 

	smoot.apple.com

### Apple Store <sup><sup>[1](https://www.reddit.com/r/nextdns/comments/xx4cwn/solutionapple_store_connection_issues)</sup></sup> 

	amp-api-edge.apps.apple.com
	amp-api-search-edge.apps.apple.com

### Windows

This [request](https://oisd.nl/excludes.php?w=settings-win.data.microsoft.com) is blocked when using NextDNS' [Native Tracking](https://github.com/yokoffing/NextDNS-Config#native-tracking-protection-1) list (Windows)

	settings-win.data.microsoft.com

### Xbox achievements

	v10.events.data.microsoft.com
	v20.events.data.microsoft.com

### Xiaomi device updates

	update.intl.miui.com

### Xiaomi USB debugging (Security settings)

	srv.sec.intl.miui.com

### Google Nest usage metrics <sup><sup>[1](https://www.reddit.com/r/nextdns/comments/yzvnuw/nest_usage_metrics_being_blocked)</sup></sup> 

	logsink.devices.nest.com

### Yahoo Mail <sup><sup>[1](https://github.com/hagezi/dns-blocklists/issues/269)</sup></sup>

	consent.yahoo.com
	guce.oath.com
	pr.comet.yahoo.com

### [Spectrum](https://spectrum.net) login <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/640)</sup></sup>

	pov.spectrum.net

### Zoom <sup><sup>[1](https://oisd.nl/excludes.php?w=log.zoom.us) [2](https://oisd.nl/excludes.php?w=us04logfiles.zoom.us)</sup></sup> 

	logfiles.zoom.us
	us04logfiles.zoom.us
	us04zpns.zoom.us

### YouTube history

	s.youtube.com

### Hulu <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/762)</sup></sup>

	ads-fa-darwin.hulustream.com

### Epic Games Launcher <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/643)</sup></sup>

	eulatracking-public-service-prod06.ol.epicgames.com

### NVIDIA Gefore Experience <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/650)</sup></sup>
	
	gfe.nvidia.com
	nvgs.nvidia.cn

### Chick-Fil-A App <sup><sup>[1](https://www.reddit.com/r/nextdns/comments/zaqio0/comment/iz7v9di/?utm_source=share&utm_medium=web2x&context=3)</sup></sup>

	tmetrix.my.chick-fil-a.com

### [imgur](https://imgur.com) <sup><sup>[1](https://github.com/lightswitch05/hosts/issues/358) [2](https://www.reddit.com/r/nextdns/comments/t3jmvk/imgur_loads_then_goes_blank_no_matter_which)</sup></sup>

	js.media-lab.ai

### [CBS](https://cbsnews.com/live) News livestream <sup><sup>[1](https://github.com/nextdns/metadata/issues/1030) [2](https://github.com/hagezi/dns-blocklists/issues/422)</sup></sup> 

	doppler-config.cbsivideo.com
	production-cmp.isgprivacy.cbsi.com
	pubads.g.doubleclick.net
	tags.tiqcdn.com 

### [Paramount+](https://www.paramountplus.com/)

Paramount+ uses certain domains to display ads. These domains must be accessible to allow Paramount+ content to load (even for viewers with ad-free plans).

:warning: However, because many sites use these domains for ads, allowing them could result in more ads being shown on other sites you visit.

    imasdk.googleapis.com
    pubads.g.doubleclick.net

Users have [reported](https://www.reddit.com/r/nextdns/comments/v84ag6/paramount_plus/) that the following domains also may need to be allowed:

    cbsaavideo.com
    cbsi.com
    conviva.com
    convivia.com
    demdex.net
    dns-clientinfo.cbsivideo.com
    partnerad.l.doubleclick.net
    saa.cbsi.com
    summerhamster.com (yes, really)
    udm.scorecardresearch.com

### [FiveThirtyEight](https://fivethirtyeight.com) videos / [National Geographic](https://nationalgeographic.com) website <sup><sup>[1](https://github.com/notracking/hosts-blocklists/issues/788)</sup></sup>

	dcf.espn.com

### [Men's Health](https://menshealth.com/nutrition/a40868905/chris-hemsworth-chicken-pasta-bake-recipe-centr) videos <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/651)</sup></sup>

	glimmer.hearstapps.com

</details>

***

# Settings :gear:

## Logs
**Storage location** → Switzerland

## Block Page
> [!CAUTION]
> Enabling this setting may cause site navigation issues if the [NextDNS Root CA](https://help.nextdns.io/t/g9hmv0a/how-to-install-and-trust-nextdns-root-ca) is not on your devices. Also, this setting breaks [Paypal 2FA](https://github.com/hagezi/dns-blocklists/issues/2335), [iCloud Private Relay](https://help.nextdns.io/t/g9hdska), [Microsoft Teams](https://www.reddit.com/r/nextdns/comments/176u2x6/comment/k4pp3ti/?context=3), [Yahoo! Mail](https://github.com/hagezi/dns-blocklists/issues/269#issuecomment-1409644343), the NAVER app, [Hoyolab app](https://help.nextdns.io/t/g9yxqcd/nextdns-blocking-hoyolab), and possibly [banking apps](https://help.nextdns.io/t/83yxjgx/most-common-problem-with-nextdns).

![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Enable Block Page

## Anonymized EDNS Client Subnet <sup><sup>[1](https://help.nextdns.io/t/m1hmv04/what-is-edns-client-subnet-ecs) </sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable Anonymized EDNS Client Subnet
## Cache Boost <sup><sup>[1](https://www.reddit.com/r/nextdns/comments/girmcf/new_setting_cache_boost/)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable Cache Boost

## CNAME Flattening <sup><sup>[1](https://medium.com/nextdns/nextdns-added-cname-uncloaking-support-becomes-the-first-cross-platform-solution-to-the-problem-e3f437f84342) [2](https://developers.cloudflare.com/dns/cname-flattening/) [3](https://advancedweb.hu/what-is-cname-flattening-and-how-it-helps-redirecting-the-apex-domain) </sup></sup>
> [!WARNING]
> Enabling this feature may break compatibility with [Yahoo! Mail](https://github.com/hagezi/dns-blocklists/issues/269#issuecomment-1409644343) and cause issues with certain blocklists.

![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Enable CNAME Flattening

## Web3 <sup><sup> [1](https://x.com/NextDNS/status/1491034351391305731) [2](https://gabygoldberg.notion.site/f7050e62461143d49345e7b46eb5576b)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable Web3 → (optional)

***
# FAQ :question:

## How do I signup for NextDNS?
Click [here](https://nextdns.io/?from=xujj63g5) to get started.

## Why am I still seeing ads?
Not all ads can be blocked at the DNS level.<sup>[1](https://www.reddit.com/r/nextdns/comments/14nsfhv/comment/jq982bi/?context=3) [2](https://www.reddit.com/r/nextdns/comments/13urdda/ads_on_manga_sites/)</sup> You will need an [ad blocker](https://github.com/yokoffing/NextDNS-Config#i-need-a-browser-with-ad-blocking-which-one-should-i-choose) to block what's leftover.

This is because not all ads come from third-party domains; some ads come directly from the site you're visiting, like [YouTube](https://discourse.pi-hole.net/t/how-do-i-block-ads-on-youtube/253/2). DNS blockers stop the resolution of a domain, and content blockers filter page content. Click [here](https://github.com/yokoffing/NextDNS-Config/tree/main#i-need-a-browser-with-ad-blocking-which-one-should-i-choose) to easily install a lightweight ad blocker.

## I need a browser with ad blocking. Which one should I choose?
Choosing a browser is about as intimate as [choosing a starter Pokémon](https://www.youtube.com/watch?v=F_8htiBjTCY), so here's a few caveats:
* The best browser on paper may not work well in real world usage.
* Browsers are tools! Use a variety of browsers depending on what you need to do.
* You should use various browsers (or browser profiles) for different areas of life (e.g., work, school, personal).

We based the recommendations below on a combination of effectiveness, resource efficiency, features, and ease of use.

| OS | Browser | Content Blocker |
|---|---|---|
| iOS | [Safari](https://www.privacyguides.org/en/mobile-browsers/#safari) | [AdGuard](https://www.privacyguides.org/en/browser-extensions/?h=adguard#adguard) |
| Android | [Brave](https://www.privacyguides.org/en/mobile-browsers/#brave) | Built-in blocker |
| Windows <br> macOS <br> Linux | [Firefox](https://www.mozilla.org/en-US/firefox/new/) (with [Betterfox](https://github.com/yokoffing/Betterfox#betterfox)) <p><p> [Brave](https://www.privacyguides.org/en/desktop-browsers/#brave) | [uBlock Origin](https://addons.mozilla.org/blog/ublock-origin-everything-you-need-to-know-about-the-ad-blocker/) <p><p> Built-in blocker or [uBlock Origin](https://addons.mozilla.org/blog/ublock-origin-everything-you-need-to-know-about-the-ad-blocker/) |  |

At the end of the day, if you're using [NextDNS](https://nextdns.io/?from=xujj63g5) + any browser with an ad blocker, you have more coverage than most people.

## Should I pay for NextDNS?
For the rich features it provides, [NextDNS](https://nextdns.io/?from=xujj63g5) is very affordable at $19.90/year for unlimited devices. NextDNS pays for itself if it saves my family from a malicious incident.

## Does the amount of features enabled affect the speed of NextDNS?<sup>[1](https://github.com/yokoffing/NextDNS-Config/issues/12#issue-1465457977) [2](https://www.reddit.com/r/nextdns/comments/135utai/comment/jilbus8/?=&context=3)</sup>

The number of settings you toggle on will not affect your DNS latency.

## Do I need to set DoH at browser-level if I already use NextDNS at system-level?
Unless you use a separate profile for the browser, it is [not neccessary](https://www.reddit.com/r/nextdns/comments/yfjvqy/is_it_redundant_to_set_at_doh_at_browserlevel_if/iu3vjzt/?context=3). However, I recommend [setting it in your web browser](https://itechtics.com/dns-over-https/#how-to-enable-or-disable-dns-over-https-in-your-browsers) anyway. 

## I have a router profile and a device profile. Which one does my device use?
The device will use the profile set by the [NextDNS](https://nextdns.io/?from=xujj63g5) app or the installed [root CA](https://help.nextdns.io/t/g9hmv0a/how-to-install-and-trust-nextdns-root-ca). However, if the device has not been configured to use a separate profile, then it will use the wifi/router configuration.<sup>[1](https://www.reddit.com/r/nextdns/comments/yf4hnv/question_about_home_router_and_app_running_in/)</sup>

## What is the difference between security, privacy, and anonymity?
See [article](https://thenewoil.org/en/guides/prologue/secprivanon/) | [video](https://www.youtube.com/watch?v=Wpkh-hfULgE)

## Does NextDNS hide activity from my Internet Service Provider (ISP)?
Encrypted DNS queries boost privacy and security. This encryption stops your ISP from seeing what websites you search for and visit.

However, encrypted DNS does not hide website IP addresses from your ISP. While your ISP cannot see the specific domain you want to access, they can see that you contact DNS servers like Cloudflare or AWS. If you repeatedly send data to a certain IP address, your ISP can guess you are visiting a website at that address.

## Do I need a VPN?
IVPN [argues](https://www.ivpn.net/blog/why-you-dont-need-a-vpn/) you only need a VPN for three reasons. Mainly, in order to:

1. Hide your real IP address from websites and peer-to-peer networks, which prevents ISPs and mobile carriers from tracking your online activity.

2. Guard against [man in the middle](https://en.wikipedia.org/wiki/Man-in-the-middle_attack) and other [common attacks](https://en.wikipedia.org/wiki/Evil_twin_(wireless_networks)) on public Wi-Fi networks in places like airports, hotels, cafes, and libraries.

3. Bypass censorship or geographic restrictions, allowing you to access blocked websites and content.

Ultimately, you don't need a VPN unless your [threat model](https://thenewoil.org/en/guides/prologue/threat-model/) demands it. Here are VPN suggestions from [Techlore](https://www.techlore.tech/vpn.html) and [Tom Spark Reviews](https://www.vpntierlist.com/vpn-tier-list-2024) if it does.

***
# Mentions :books:

### User Comments
* See [here](https://socialgrep.com/search?query=yokoffing%2Cnextdns)

### YouTube
* [The ULTIMATE Guide to Mastering NextDNS!](https://www.youtube.com/watch?v=WUG57ynLb8I&t=2230s) | [clarifications](https://github.com/techlore/channel-content/issues/43) (July 2023) 

### Articles
* [Knot Resolver — with ad blocking](https://blog.cavelab.dev/2022/12/knot-resolver-ad-blocking/) (Dec 2022)
* [Privacy Toolkit: NextDNS](https://stephenbolen.com/privacy-toolkit-nextdns/#:~:text=I%20found%20a%20wonderful%20guide%20on%20GitHub%20that%20walks%20through%20the%20optimal%20NextDNS%20configuration) (Sept 2022)

### Guides
* [A comprehensive guide to setting up NextDNS](https://itsjake.me/blog/a-comprehensive-guide-to-setting-up-nextdns/) (Sept 2023)
* [FMHY: DNS Adblocking](https://github.com/nbats/FMHYedit/blob/main/AdblockVPNGuide.md#-dns-adblocking) → NextDNS → Guide
* [hagezi/dns-blocklists](https://github.com/hagezi/dns-blocklists#department_store-nextdns---limited-freepaid-) → Online DNS Services

### Contributions
* [Hagezi](https://github.com/hagezi/dns-blocklists/issues?q=author%3Ayokoffing) | [mentions](https://github.com/hagezi/dns-blocklists/issues?q=mentions%3Ayokoffing)
* [1Hosts](https://github.com/badmojr/1Hosts/issues?q=author%3Ayokoffing)
* [Easylist](https://github.com/easylist/easylist/issues?q=author%3Ayokoffing)
* [uBlock Origin](https://github.com/uBlockOrigin/uAssets/issues?q=author%3Ayokoffing)
* [AdGuard](https://github.com/AdguardTeam/AdguardFilters/issues?q=author%3Ayokoffing)

<div align='center'><a href='https://websitecounterfree.com'><img src='https://websitecounterfree.com/c.php?d=9&id=19651&s=1' border='0' alt='Free Website Counter'></a><br / ></div>
<div align='center'>since 23 July 2022</div>
