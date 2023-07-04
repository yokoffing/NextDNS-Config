[![GitHub issues](https://img.shields.io/github/issues/yokoffing/NextDNS-Config)](https://github.com/yokoffing/NextDNS-Config/issues)
![GitHub repo size](https://img.shields.io/github/repo-size/yokoffing/NextDNS-Config)
![GitHub](https://img.shields.io/github/license/yokoffing/NextDNS-Config?color=blue)
![GitHub Maintained](https://img.shields.io/badge/Open%20Source-Yes-green)
![GitHub commit activity](https://img.shields.io/github/commit-activity/y/yokoffing/NextDNS-Config)
![GitHub last commit](https://img.shields.io/github/last-commit/yokoffing/NextDNS-Config)
![GitHub Maintained](https://img.shields.io/badge/maintained-yes-green)
[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fyokoffing%2FNextDNS-Config&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

***
# Guidelines :bookmark:
1) Prevent overblocking by utilizing the [law of diminishing returns](https://pmctraining.com/site/wp-content/uploads/2018/04/Law-of-Diminishing-Returns-CHART.png) (e.g., using [sane](https://privacyguides.org/basics/threat-modeling), quality [blocklists](https://github.com/yokoffing/NextDNS-Config#blocklists-1); allowing most [TLDs](https://github.com/yokoffing/NextDNS-Config#block-top-level-domains-tlds-1-2-3-4-5-); etc.).
2) Pass the [girlfriend test](https://urbandictionary.com/define.php?term=Grandma%20Test) with few exceptions. These deviations are documented throughout the guide.

***

## Create your account

Sign up for NextDNS [here](https://nextdns.io/?from=xujj63g5)!

***

# Security :police_officer:

Security settings protect your data from harm, theft, and unauthorized use.<sup>*^[why does this matter?](https://thenewoil.org/en/guides/prologue/why)*</sup>

### Threat Intelligence Feeds <sup><sup>[1](https://github.com/nextdns/metadata/blob/6f9b6cd0670e7e31ad2ca716742088c2fc0616c2/security/threat-intelligence-feeds.json)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Use Threat Intelligence Feeds
### AI-Driven Threat Detection <sup><sup>[1](https://unofficialbird.com/NextDNS/status/1440291577713233925?lang=en)</sup></sup>
:warning: This feature is still in beta and may cause [false positives](https://csrc.nist.gov/glossary/term/false_positive).
<br><br>![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Enable AI-Driven Threat Detection
### Google Safe Browsing <sup><sup> [1](https://safebrowsing.google.com/safebrowsing/report_general/) [2](https://blog.cryptographyengineering.com/2019/10/13/dear-apple-safe-browsing-might-not-be-that-safe/) [3](https://the8-bit.com/apple-proxies-google-safe-browsing-privacy/) [4](https://github.com/brave/brave-browser/wiki/Deviations-from-Chromium-(features-we-disable-or-remove)#services-we-proxy-through-brave-servers) </sup></sup>
:bulb: Unlike the version embedded in some browsers, this does not associate your public IP address to threats and does not allow bypassing the block. <p>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable Google Safe Browsing
### Cryptojacking Protection <sup><sup>[1](https://github.com/nextdns/metadata/blob/6f9b6cd0670e7e31ad2ca716742088c2fc0616c2/security/cryptojacking.json)</sup></sup>
:warning: If you use something other than the [recommended blocklists](https://github.com/yokoffing/NextDNS-Config#privacy-lock), then you should [leave this enabled](https://github.com/yokoffing/NextDNS-Config/issues/31).
<br><br>![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Enable Cryptojacking Protection
### DNS Rebinding Protection <sup><sup>[1](https://help.nextdns.io/t/35hmval/what-is-dns-rebinding-protection) [2](https://www.reddit.com/r/nextdns/comments/t0ne8r/does_dns_rebinding_protection_block_remote_access/?context=3)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg)  Enable DNS Rebinding Protection
### IDN Homograph Attacks Protection <sup><sup>[1](https://blog.riotsecurityteam.com/idn-homograph-attacksprevention) [2](https://akamai.com/blog/security/watch-your-step-the-prevalence-of-idn-homograph-attacks)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable Homograph Attacks Protection
### Typosquatting Protection <sup><sup>[1](https://github.com/nextdns/metadata/blob/6f9b6cd0670e7e31ad2ca716742088c2fc0616c2/security/typosquatting/protected-domains)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable Typosquatting Protection
### Domain Generation Algorithms (DGAs) Protection
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable DGA Protection
### Block Newly Registered Domains (NRDs) <sup><sup>[1](https://boldgrid.com/instagram-influencer-accounts-are-being-hacked-phishing-attacks) </sup></sup>
:warning: Blocking NRDs may cause [false positives](https://csrc.nist.gov/glossary/term/false_positive) [occasionally](https://www.reddit.com/r/InternetIsBeautiful/comments/w2wdro/comment/iguvg8y/?context=3). Be selective when adding NRDs to your allowlist; and, if you do, **NEVER** give [sensitive information](https://egnyte.com/guides/governance/sensitive-information) to a NRD. *If you plan to [set-and-forget](https://glosbe.com/en/en/set-and-forget) your configuration, disable this setting.*
<br><br>![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Block Newly Registered Domains (NRDs)
### Block Dynamic DNS Hostnames <sup><sup>[1](https://github.com/nextdns/ddns-domains/blob/main/suffixes) [2](https://unofficialbird.com/NextDNS/status/1541740963760144386) </sup></sup>
:warning: This feature is still in beta and may cause [false positives](https://csrc.nist.gov/glossary/term/false_positive). <p>
:bulb: If you are using Dynamic DNS (DDNS), this setting will **not** block the DDNS services' own website or their update API. <p>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable Block Dynamic DNS Hostnames
### Block Parked Domains <sup><sup>[1](https://github.com/nextdns/metadata/blob/6f9b6cd0670e7e31ad2ca716742088c2fc0616c2/security/parked-domains-cname)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Block Parked Domains
### Block Top-Level Domains (TLDs) <sup><sup>[1](https://webtribunal.net/blog/tld-statistics/) [2](https://www.spamhaus.org/statistics/tlds/) [3](https://bleepingcomputer.com/news/security/verified-twitter-accounts-hacked-to-send-fake-suspension-notices/) [4](https://github.com/DandelionSprout/adfilt/blob/master/Dandelion%20Sprout's%20Anti-Malware%20List.txt) [5](https://github.com/DandelionSprout/adfilt/issues/659#issuecomment-1284845803) </sup></sup>
:warning: Blocking [TLDs](https://geeksforgeeks.org/components-of-a-url) may cause [false positives](https://csrc.nist.gov/glossary/term/false_positive) since this feature blocks both site nagviations and subrequests. However, the entries below should allow for everyday browsing while offering protection against commonly abused TLDs since they have no known legitimate uses.

```

.cfd
.discount
.gdn
.loan
.loans
.ooo
.sbs
.zip
```

:stop_sign: Below are additional TLDs you may block, but you may need to [allowlist](https://github.com/yokoffing/NextDNS-Config#allowlist-white_check_mark) sites on occasion. *If you plan to [set-and-forget](https://glosbe.com/en/en/set-and-forget) your configuration, skip this setting.*

<details>

```
.fit
.surf
.cn
.monster
---
.agency
.bid
.buzz
.cf
.dad
.esq
.foo
.ga
.gq
.ml
.mov
.nexus
.phd
.prof
.pw
.ru
.tk
.top
.zone
```

</details>

:memo: If you would rather block TLDs with an adblocker (e.g., easier to troubleshoot breakage), add the first two filterlists [here](https://github.com/yokoffing/filterlists#security).

### Block Child Sexual Abuse Material
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Block Child Sexual Abuse Material

***

# Privacy :lock:
Privacy features limit the amount of data companies can collect about you.

Because privacy is a [spectrum](https://blog.thenewoil.org/the-privacy-myth-binary-vs-spectrum), what you need varies on your [threat model](https://thenewoil.org/en/guides/prologue/threatmodel), interest, and skillset.<sup>^[*why should I care? I have nothing to hide*](https://aeon.co/essays/privacy-matters-because-it-empowers-us-all)</sup>

### Blocklists <sup><sup>[1](https://github.com/nextdns/blocklists/tree/main/blocklists)</sup></sup>

Blocklists filter out ads, [trackers](https://freecodecamp.org/news/what-you-should-know-about-web-tracking-and-how-it-affects-your-online-privacy-42935355525/), and malicious sites. Hundreds of volunteers contribute to these lists in the [open-source](https://opensource.com/resources/what-open-source) community, and they are the undercover heroes who make blocking ads at scale possible.

We recommend you remove the [NextDNS Ads & Trackers Blocklist](https://github.com/nextdns/blocklists/blob/main/blocklists/nextdns-recommended.json) and select the [minimum](https://www.reddit.com/r/nextdns/comments/1048xeg/do_you_use_nextdns_blocklist_as_the_primary/j33wnz2/?context=3) number of useful lists.

#### Which blocklist should I use?

A great question to ask is: "How much do I want to deal with the inconveniences of [false positives](https://csrc.nist.gov/glossary/term/false_positive)?"

Here are the suggested blocklists:

|     **Blocklist**    |                              **Rationale**                                             |
|:--------------------:|:--------------------------------------------------------------------------------------:|
| HaGeZi - Multi **LIGHT** | Block most tracker and ad requests without issues ([set-and-forget](https://glosbe.com/en/en/set-and-forget)) |
| HaGeZi - Multi **PRO++** | Block 9-15% more requests <br> Occasionally allowlist requests for [email unsubscriptions](https://www.reddit.com/r/nextdns/comments/y3zmhb/new_on_nextdns_and_im_loving_it_any_advices_about/ish8dla/?context=1) <br> [Submit](https://github.com/hagezi/dns-blocklists/issues/new/choose) occasional site and app issues |

:book: Read the full analysis of Hagezi's lists [here](https://github.com/hagezi/dns-blocklists/discussions/1093).

:bulb: Use different blocklists on separate DNS profiles (e.g., LIGHT for your router and PRO++ for your web browser).

#### Why Hagezi?
[Hagezi](https://github.com/hagezi/dns-blocklists) block ads, trackers, native device trackers, badware, and more. He maintains a sensible allowlist, handles false positives quickly, an communicates known issues to blocklists maintainers. Hagezi's primary DNS lists combine respected community blocklists like [OISD](https://oisd.nl/), [Steven Black](https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts), [1Hosts](https://github.com/badmojr/1Hosts#safeguard-your-devices-against-pesky-ads-trackers-and-malware), [notrack](https://gitlab.com/quidsup/notrack#notrack), and [more](https://github.com/hagezi/dns-blocklists/blob/main/usedsources.md#proplus).

:question: You may wonder why other lists are not utilized. This is because many list maintainers:
* do not remove [false positives](https://csrc.nist.gov/glossary/term/false_positive) and/or are no longer active <sup>[1](https://github.com/lightswitch05/hosts/issues/356) [2](https://github.com/EnergizedProtection/block/issues/916)</sup>
* already [aggregate](https://www.reddit.com/r/nextdns/comments/ys3s1s/confused_about_blocklists/ivxdcd2/?context=3) common blocklists into their own list (Easylist/Fanboy, AdGuard, Steven Black, etc.) <sup>[1](https://github.com/badmojr/1Hosts/blob/master/-data/lists/assets.txt) [2](https://oisd.nl/includedlists/big/0) [3](https://github.com/jerryn70/GoodbyeAds/blob/master/Docs/Sources.md) [4](https://github.com/hagezi/dns-blocklists/blob/main/usedsources.md#proplus) </sup>
* offer no meaningful additional coverage when compared with the chart combinations above

### Native Tracking Protection <sup><sup>[1](https://github.com/nextdns/native-tracking-domains/tree/main/domains)</sup></sup>

Add all the device brands you use. There's no advantage in adding brands you don't have; however, there’s no disadvantage in adding unused brands, either.

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

### Block Disguised Third-Party Trackers <sup><sup>[1](https://github.com/nextdns/cname-cloaking-blocklist/blob/master/domains) [2](https://www.reddit.com/r/nextdns/comments/10nenu3/disguised_trackers_are_blocked_regardless_of) [3](https://medium.com/nextdns/cname-cloaking-the-dangerous-disguise-of-third-party-trackers-195205dc522a) [4](https://arxiv.org/pdf/2102.09301.pdf) [5](https://tma.ifip.org/2020/wp-content/uploads/sites/9/2020/06/tma2020-camera-paper66.pdf) </sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Block Disguised Third-Party Trackers

### Allow Affiliate & Tracking Links <sup><sup>[1](https://github.com/nextdns/click-tracking-domains) [2](https://unofficialbird.com/NextDNS/status/1539229377560461312) </sup></sup>
:bulb: Your IP address will automatically be hidden (via [TCP](https://educba.com/what-is-tcp-ip) [proxying](https://en.wikipedia.org/wiki/Proxy_server#/media/File:Proxy_concept_en.svg)) to preserve your privacy.<p>
:warning: Disabling causes [false positives](https://csrc.nist.gov/glossary/term/false_positive) when opening some email links. <p>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Allow Affiliate & Tracking Links

***

# Parental Control :family_man_woman_boy:
### YouTube Restricted Mode
![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Enforce YouTube Restricted Mode
### Block Bypass Methods <sup><sup>[1](https://github.com/nextdns/dns-bypass-methods)</sup></sup>
:warning: Enabling may cause unintended breakage. <p>
![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Block Bypass Methods

***

# Denylist :no_entry:

Denylist entries are always blocked. The entries below may further harden some profiles while not interfering with everyday browsing.

<details>

### Apple tracking domains <sup><sup>[1](https://unofficialbird.com/mysk_co/status/1588308341780262912) [2](https://github.com/nextdns/metadata/pull/1132) [3](https://github.com/badmojr/1Hosts/issues/536) [4](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558)</sup></sup>
Not currently in NextDNS's [Native Tracking Protection](https://github.com/yokoffing/NextDNS-Config#native-tracking-protection-1) [list](https://github.com/nextdns/metadata/blob/6f9b6cd0670e7e31ad2ca716742088c2fc0616c2/privacy/native/apple): <sup>[1](https://raw.githubusercontent.com/hagezi/dns-blocklists/main/wildcard/native.apple.txt)</sup>

	xp.apple.com (unblock for device updates!)
	acfeedbackws.icloud.com
	api-adservices.apple.com
	feedbackws.fe.apple-dns.net
	feedbackws.icloud.com
	iadsdk.apple.com
	notes-analytics-events.apple.com
	notes-analytics-events.news.apple-dns.net
	weather-analytics-events.apple.com
	weather-analytics-events.news.apple-dns.net
	
### Twitter tracker

	syndication.twitter.com

### NVIDIA Gefore Experience <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/650)</sup></sup>

	events.gfe.nvidia.com

</details>

***

# Allowlist :white_check_mark:

Allowlist entries always resolve. These entries may be needed for aggressive DNS profiles to relax their rules.

<details>

### NextDNS

Just in case a filterlist goes [haywire](https://help.nextdns.io/t/m1hs207/energized-ultimate-lists-blocking-nextdns) and blocks your access

	nextdns.io

### Facebook / Instagram <sup><sup>[1](https://github.com/jerryn70/GoodbyeAds/issues/309)</sup></sup> 

	graph.facebook.com
	graph.instagram.com
	i.instagram.com
	b-graph.facebook.com

If you're still having issues, try [these](https://raw.githubusercontent.com/hagezi/dns-data-collection/main/share/facebook.txt):
	
	connect.facebook.com
	connect.facebook.net
	graph-fallback.facebook.com
	z-m-graph.facebook.com
	graph-fallback.instagram.com

### Apple device updates <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/536) [2](https://github.com/badmojr/1Hosts/issues/562) [3](https://github.com/nextdns/metadata/pull/1132#issuecomment-1331733770) [4](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558)

A [known tracking domain](https://gizmodo.com/apple-iphone-analytics-tracking-even-when-off-app-store-1849757558), but it's needed for device updates

	xp.apple.com

### Apple iMessage GIFs <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/560)</sup></sup> / Spotlight Search <sup><sup>[2](https://github.com/badmojr/1Hosts/issues/562)</sup></sup> 

	smoot.apple.com

### Apple Store <sup><sup>[1](https://www.reddit.com/r/nextdns/comments/xx4cwn/solutionapple_store_connection_issues)</sup></sup> 

	amp-api-edge.apps.apple.com
	amp-api-search-edge.apps.apple.com

### Windows

This [request](https://oisd.nl/excludes.php?w=settings-win.data.microsoft.com) is blocked when using NextDNS' [Native Tracking](https://github.com/yokoffing/NextDNS-Config#native-tracking-protection-1) list (Windows)

	settings-win.data.microsoft.com

### Xiaomi device updates <sup><sup>[1](https://blocklist-tools.developerdan.com/entries/search?q=update.intl.miui.com)</sup></sup> 

	update.intl.miui.com

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

### YouTube history <sup><sup>[1](https://blocklist-tools.developerdan.com/entries/search?q=s.youtube.com)</sup></sup> 

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

### [FiveThirtyEight](https://fivethirtyeight.com) videos / [National Geographic](https://nationalgeographic.com) website <sup><sup>[1](https://github.com/notracking/hosts-blocklists/issues/788)</sup></sup>

	dcf.espn.com

### [Men's Health](https://menshealth.com/nutrition/a40868905/chris-hemsworth-chicken-pasta-bake-recipe-centr) videos <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/651)</sup></sup>

	glimmer.hearstapps.com

### [Ghostery](https://ghostery.com/ghostery-ad-blocker) Analytics (opt-in)

User data is [removed](https://0x65.dev/blog/2019-12-04/human-web-proxy-network-hpn.html). Contributes to the [Human Web](https://0x65.dev/blog/2019-12-03/human-web-collecting-data-in-a-socially-responsible-manner.html) and [WhoTracks.me](https://whotracks.me) data

	collector-hpn.ghostery.net
	collector-hpn.privacy.ghostery.net
	d.ghostery.com


</details>

***

# Settings :gear:

### Logs
**Storage location** → Switzerland

### Block Page
:warning: Enabling may cause breakage if the [NextDNS Root CA](https://help.nextdns.io/t/g9hmv0a/how-to-install-and-trust-nextdns-root-ca) is not on your devices. This setting also [breaks](https://help.nextdns.io/t/g9hdska) iCloud [Private Relay](https://support.apple.com/en-us/HT212614), [Yahoo! Mail](https://github.com/hagezi/dns-blocklists/issues/269#issuecomment-1409644343), and the [NAVER](https://channelsearch.naver.com) app.
<br><br> ![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Enable Block Page
### Anonymized EDNS Client Subnet <sup><sup>[1](https://help.nextdns.io/t/m1hmv04/what-is-edns-client-subnet-ecs) </sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable Anonymized EDNS Client Subnet
### Cache Boost <sup><sup>[1](https://www.reddit.com/r/nextdns/comments/girmcf/new_setting_cache_boost/)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable Cache Boost
### CNAME Flattening <sup><sup>[1](https://medium.com/nextdns/nextdns-added-cname-uncloaking-support-becomes-the-first-cross-platform-solution-to-the-problem-e3f437f84342) [2](https://developers.cloudflare.com/dns/additional-options/cname-flattening) [3](https://advancedweb.hu/what-is-cname-flattening-and-how-it-helps-redirecting-the-apex-domain) </sup></sup>
:warning: Enabling may cause [breakage with Yahoo! Mail](https://github.com/hagezi/dns-blocklists/issues/269#issuecomment-1409644343) and cause issues with some blocklists.
<br><br> ![Disabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/disabled.svg) Enable CNAME Flattening
### Web3 <sup><sup> [1](https://unofficialbird.com/NextDNS/status/1491034351391305731) [2](https://gabygoldberg.notion.site/f7050e62461143d49345e7b46eb5576b)</sup></sup>
![Enabled](https://raw.githubusercontent.com/yokoffing/NextDNS-Config/main/icons/enabled.svg) Enable Web3 → (optional)

***
# FAQ :question:

### How do I signup for NextDNS?
Click [here](https://nextdns.io/?from=xujj63g5)!

### Should I pay for NextDNS?
For the rich features it provides, [NextDNS](https://nextdns.io/?from=xujj63g5) is very affordable at $19.90/year for unlimited devices. NextDNS pays for itself if it saves my family from a malicious incident.

### Why am I still seeing ads?
Not all ads can be blocked at the DNS level.<sup>[1](https://www.reddit.com/r/nextdns/comments/14nsfhv/comment/jq982bi/?context=3) [2](https://www.reddit.com/r/nextdns/comments/13urdda/ads_on_manga_sites/)</sup> You will need an [ad blocker](https://github.com/yokoffing/NextDNS-Config#i-need-a-browser-with-ad-blocking-which-one-should-i-choose) to block what's leftover.

This is because not all ads come from third-party domains; some ads come directly from the site you're visiting, like [YouTube](https://discourse.pi-hole.net/t/how-do-i-block-ads-on-youtube/253/2). DNS blockers [stop](https://github.com/hagezi/dns-blocklists/discussions/1030#discussioncomment-5884270) the resolution of a domain, and content blockers filter page content. Click [here](https://github.com/yokoffing/NextDNS-Config/tree/main#i-need-a-browser-with-ad-blocking-which-one-should-i-choose) to easily install a lightweight ad blocker.

### Does the amount of features enabled affect the speed of NextDNS?<sup>[1](https://github.com/yokoffing/NextDNS-Config/issues/12#issue-1465457977) [2](https://www.reddit.com/r/nextdns/comments/135utai/comment/jilbus8/?=&context=3)</sup>

The number of settings you toggle on will not affect your DNS latency.

### Do I need to set DoH at browser-level if I already use NextDNS at system-level?
Unless you use a separate profile for the browser, it is [not neccessary](https://www.reddit.com/r/nextdns/comments/yfjvqy/is_it_redundant_to_set_at_doh_at_browserlevel_if/iu3vjzt/?context=3). However, I recommend [setting it in your web browser](https://itechtics.com/dns-over-https/#how-to-enable-or-disable-dns-over-https-in-your-browsers) anyway. 

### I have a router profile and a device profile. Which one does my device use?
The device will use the profile set by the [NextDNS](https://nextdns.io/?from=xujj63g5) app or the installed [root CA](https://help.nextdns.io/t/g9hmv0a/how-to-install-and-trust-nextdns-root-ca). However, if the device has not been configured to use a separate profile, then it will use the wifi/router configuration.<sup>[1](https://www.reddit.com/r/nextdns/comments/yf4hnv/question_about_home_router_and_app_running_in/)</sup>

### What is the difference between security, privacy, and anonymity?
See [article](https://thenewoil.org/en/guides/prologue/secprivanon/) | [video](https://youtu.be/Wpkh-hfULgE)

### Does NextDNS hide activity from my Internet Service Provider (ISP)?
[No](https://www.reddit.com/r/nextdns/comments/tavcgm/comment/i039u1r/?context=3). [NextDNS](https://nextdns.io/?from=xujj63g5) is only concerned about DNS traffic. You would need a [quality](https://www.youtube.com/watch?v=cK4MQv-OwyM) [VPN](https://www.ivpn.net/blog/why-you-dont-need-a-vpn/) to hide all activity from your ISP.

### I need a browser with ad blocking. Which one should I choose?
Choosing a browser is about as intimate as [choosing a starter Pokémon](https://youtu.be/F_8htiBjTCY), so here's a few caveats:
* The best browser on paper may not work well in real world usage (e.g., [Brave](https://brave.com/) is wonky with video playback on iOS).
* Browsers are tools! Use a variety of browsers depending on what you need to do.
* You should use various browsers (or browser profiles) for different areas of life (e.g., work, school, personal).

We based the recommendations below on a combination of effectiveness, resource efficiency, features, and ease of use.

Here are the suggested browsers for each operating system (OS):

#### Mobile

| OS | Browser | Content Blocker | Notes |
|---|---|---|---|
| iOS | [Safari](https://www.apple.com/safari) <br>[Orion](https://browser.kagi.com/) | [Ghostery](https://www.ghostery.com/ghostery-ad-blocker-safari) | [AdGuard](https://adguard.com/en/adguard-ios/overview.html) allows you to add custom filterlists but it's resource intensive.  |
| Android | Firefox | [Ghostery](https://www.ghostery.com/ghostery-ad-blocker-firefox) or [uBlock Origin](https://addons.mozilla.org/blog/ublock-origin-everything-you-need-to-know-about-the-ad-blocker/) |  |

#### Desktop

| OS | Browser | Content Blocker |
|---|---|---|
| Any | [Firefox](https://www.mozilla.org/en-US/firefox/new/) (with [Betterfox](https://github.com/yokoffing/Betterfox#betterfox)) | [Ghostery](https://www.ghostery.com) or [uBlock Origin](https://addons.mozilla.org/blog/ublock-origin-everything-you-need-to-know-about-the-ad-blocker/) |  |

***
# Mentions :books:

### User Comments
* See [here](https://socialgrep.com/search?query=yokoffing%2Cnextdns)

### YouTube
* [The ULTIMATE Guide to Mastering NextDNS!](https://youtu.be/WUG57ynLb8I?t=2230) (July 2023) | [clarifications](https://github.com/techlore/channel-content/issues/43)

### Articles
* [Knot Resolver — with ad blocking](https://blog.cavelab.dev/2022/12/knot-resolver-ad-blocking/) (Dec 2022)
* [Privacy Toolkit: NextDNS](https://stephenbolen.com/privacy-toolkit-nextdns/#:~:text=I%20found%20a%20wonderful%20guide%20on%20GitHub%20that%20walks%20through%20the%20optimal%20NextDNS%20configuration) (Sept 2022)

### Guides
* [FMHY: DNS Adblocking](https://github.com/nbats/FMHYedit/blob/main/AdblockVPNGuide.md#-dns-adblocking) → NextDNS → Guide
* [hagezi/dns-blocklists](https://github.com/hagezi/dns-blocklists#nextdns---limited-freepaid-) → Online DNS services

### Contributions
* [Hagezi](https://github.com/hagezi/dns-blocklists/issues?q=author%3Ayokoffing) | [mentions](https://github.com/hagezi/dns-blocklists/issues?q=mentions%3Ayokoffing)
* [1Hosts](https://github.com/badmojr/1Hosts/issues?q=author%3Ayokoffing)
* [Easylist](https://github.com/easylist/easylist/issues?q=author%3Ayokoffing)
* [uBlock Origin](https://github.com/uBlockOrigin/uAssets/issues?q=author%3Ayokoffing)
* [AdGuard](https://github.com/AdguardTeam/AdguardFilters/issues?q=author%3Ayokoffing)

<div align='center'><a href='https://websitecounterfree.com'><img src='https://websitecounterfree.com/c.php?d=9&id=19651&s=1' border='0' alt='Free Website Counter'></a><br / ></div>
<div align='center'>since 23 July 2022</div>
