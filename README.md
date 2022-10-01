[![GitHub issues](https://img.shields.io/github/issues/yokoffing/NextDNS-Config)](https://github.com/yokoffing/NextDNS-Config/issues)
[![GitHub closed issues](https://badgen.net/github/closed-issues/yokoffing/NextDNS-Config?color=green)](https://github.com/yokoffing/NextDNS-Config/issues?q=is%3Aissue+is%3Aclosed)
![GitHub repo size](https://img.shields.io/github/repo-size/yokoffing/NextDNS-Config)
![GitHub](https://img.shields.io/github/license/yokoffing/NextDNS-Config?color=blue)
![GitHub Maintained](https://img.shields.io/badge/Open%20Source-Yes-green)
![GitHub commit activity](https://img.shields.io/github/commit-activity/y/yokoffing/NextDNS-Config)
![GitHub last commit](https://img.shields.io/github/last-commit/yokoffing/NextDNS-Config)
![GitHub Maintained](https://img.shields.io/badge/maintained-yes-green)
[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fyokoffing%2FNextDNS-Config&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

***
# Guidelines :bookmark:
1) Prevent overblocking by utilizing the [law of diminishing returns](https://pmctraining.com/site/wp-content/uploads/2018/04/Law-of-Diminishing-Returns-CHART.png) (e.g., using [sane](https://www.privacyguides.org/basics/threat-modeling/), quality [blocklists](https://github.com/yokoffing/NextDNS-Config#blocklists-1); allowing most [TLDs](https://github.com/yokoffing/NextDNS-Config#block-top-level-domains-tlds-1-2-3-4-5); etc.).
2) Pass the [girlfriend test](https://www.urbandictionary.com/define.php?term=Grandma%20Test) with few exceptions. These deviations are documented throughout the guide.

***

# Security :policeman:

Security settings protect your data from harm, theft, and unauthorized use.

### Threat Intelligence Feeds <sup><sup>[1](https://github.com/nextdns/metadata/blob/master/security/threat-intelligence-feeds.json)</sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Use Threat Intelligence Feeds
### AI-Driven Threat Detection
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable AI-Driven Threat Detection
### Google Safe Browsing <sup><sup> [1](https://user-images.githubusercontent.com/11689349/107696360-d8dde800-6c7f-11eb-9882-cccc8d2065c5.jpg) [2](https://the8-bit.com/apple-proxies-google-safe-browsing-privacy/) [3](https://github.com/brave/brave-browser/wiki/Deviations-from-Chromium-(features-we-disable-or-remove)#services-we-proxy-through-brave-servers) </sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Google Safe Browsing
### Cryptojacking Protection <sup><sup>[1](https://github.com/nextdns/metadata/blob/master/security/cryptojacking.json)</sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Cryptojacking Protection
### DNS Rebinding Protection <sup><sup>[1](https://help.nextdns.io/t/35hmval/what-is-dns-rebinding-protection) [2](https://www.reddit.com/r/nextdns/comments/t0ne8r/does_dns_rebinding_protection_block_remote_access/?context=3)</sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg)  Enable DNS Rebinding Protection
### IDN Homograph Attacks Protection
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Homograph Attacks Protection
### Typosquatting Protection <sup><sup>[1](https://github.com/nextdns/metadata/blob/master/security/typosquatting/protected-domains)</sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Typosquatting Protection
### Domain Generation Algorithms (DGAs) Protection
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable DGA Protection
### Block Newly Registered Domains (NRDs) <sup><sup>[1](https://www.malwarebytes.com/glossary/phishing) [2](https://old.reddit.com/r/uBlockOrigin/comments/w64sqt/comment/ihboutk/?context=3) [3](https://www.boldgrid.com/instagram-influencer-accounts-are-being-hacked-phishing-attacks/) </sup></sup>
:warning: Blocking NRDs may cause [false positives](https://csrc.nist.gov/glossary/term/false_positive) [occasionally](https://old.reddit.com/r/InternetIsBeautiful/comments/w2wdro/comment/iguvg8y/?context=3). Be selective when adding NRDs to your allowlist; and, if you do, **NEVER** give [sensitive information](https://www.egnyte.com/guides/governance/sensitive-information) to a NRD. *If you plan to [set-and-forget](https://glosbe.com/en/en/set-and-forget) your configuration, disable this setting.*
<br><br>![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Block Newly Registered Domains (NRDs)
### Block Dynamic DNS Hostnames <sup><sup>[1](https://github.com/nextdns/metadata/blob/master/security/ddns/suffixes) [2](https://twitter.com/NextDNS/status/1541740963760144386?cxt=HHwWhIC8iZ7PruUqAAAA) [3](https://www.phishing.org/what-is-phishing) </sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Block Dynamic DNS Hostnames
### Block Parked Domains <sup><sup>[1](https://github.com/nextdns/metadata/blob/master/security/parked-domains-cname)</sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Block Parked Domains
### Block Top-Level Domains (TLDs) <sup><sup>[1](https://webtribunal.net/blog/tld-statistics/) [2](https://www.spamhaus.org/statistics/tlds/) [3](https://www.bleepingcomputer.com/news/security/verified-twitter-accounts-hacked-to-send-fake-suspension-notices/) [4](https://github.com/iam-py-test/my_filters_001/blob/main/enhanced_protection.txt) </sup></sup>
:warning: Blocking [TLDs](https://www.geeksforgeeks.org/components-of-a-url/) can cause [false positives](https://csrc.nist.gov/glossary/term/false_positive). Some TLDs may be unusable if you visit many websites that use them. Add websites affected to your [allowlist](https://github.com/yokoffing/NextDNS-Config#allowlist-white_check_mark) if they are not malicious. Blocking the following TLDs should allow for everyday browsing while providing a boost to security; however, you may need to allowlist a website on occasion. *If you plan to [set-and-forget](https://glosbe.com/en/en/set-and-forget) your configuration, skip this setting.*
	
```
.work
.fit
.surf
.tokyo
.cn
-
.agency
.associates
.bid
.buzz
.cam
.casa
.cf
.ci
.cricket
.discount
.financial
.fit
.fun
.ga
.gq
.icu
.live
.loan
.ml
.monster
.online
.ooo
.rest
.shop
.tk
.top
.wang
.webcam
.win
```

:radioactive: If you use [NX Enhanced](https://github.com/hjk789/NXEnhanced#nx-enhanced) and want to [block most TLDs](https://github.com/hjk789/NXEnhanced#security-page), then be sure to allow for these common ones:

<details>
	
```
.review
.info
-
.au
.biz (optional)
.ca
.co
.com
.cz (optional)
.de
.dev
.download
.edu
.email
.eu
.fr
.gg
.goog
.gov
.io
.ir
.it
.jp
.ly
.me
.mil
.mobi
.ne
.net
.news
.nl
.org
.page
.ru
.site
.to
.tube (optional)
.tv
.ua
.us
.video (optional)
.website
.xxx (optional)
.xyz
```

</details>
 
### Block Child Sexual Abuse Material
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Block Child Sexual Abuse Material

***

# Privacy :lock:
Privacy features block certain requests so that companies cannot track your information and browsing history.

Privacy is a [spectrum](https://blog.thenewoil.org/the-privacy-myth-binary-vs-spectrum). What you need varies on your [threat model](https://thenewoil.org/threatmodel.html), interest, and skillset. (You can watch [this short video](https://youtu.be/Wpkh-hfULgE) to understand the difference between security and privacy.)

### Blocklists <sup><sup>[1](https://github.com/nextdns/metadata/tree/master/privacy/blocklists)</sup></sup>

Blocklists are community generated lists that block ads and [trackers](https://www.freecodecamp.org/news/what-you-should-know-about-web-tracking-and-how-it-affects-your-online-privacy-42935355525/). Filters can be categorized into five tiers of coverage:
1) **None**: no breakage; NextDNS still protects against malicious threats (à la [security settings](https://github.com/yokoffing/NextDNS-Config#security-cop)) but will allow ads and trackers
2) **Basic**: rare breakage; prioritizes functionality over blocking; *very* forgiving; ideal for router profiles
3) **Balanced**: minimal breakage; should not interfere with everyday browsing; largely [set-and-forget](https://glosbe.com/en/en/set-and-forget) but you may need to allowlist occasionally
4) **Strict**: moderate breakage; prioritizes privacy over user experience; must [manage your allowlist](https://github.com/yokoffing/NextDNS-Config#allowlist-white_check_mark) regularly
5) **Aggressive**: excessive breakage; use on a separate profile to [lockdown single-purpose devices](https://old.reddit.com/r/nextdns/comments/uqap3n/comment/i8q8alf/?context=3)

Here's a compliation of popular blocklists available in NextDNS:

|	Basic				|            Balanced	              	|            Strict		      	|            Aggressive    	        	|
|:---------------------------------: 	|:---------------------------------:	|:------------------------------:	|:----------------------------------------:	|
|	1Hosts (mini)			|           1Hosts (Lite)           	|	1Hosts (Pro) 	         	|               1Hosts (Xtra)              	|
|	oisd				|             oisd			| NextDNS Ads & Trackers Blocklist	|		Goodbye Ads		  	|
|					| 	NoTrack Tracker Blocklist    	| Lightswitch05 - Ads & Tracking	|		Energized Ultimate		|

:bulb: The **Balanced** tier is recommended for the average user, based on my testing and user feedback.<sup>[1](https://old.reddit.com/r/nextdns/comments/s2gzc5/oisd_vs_1hostsminiliteproxtra/hsgmp5n/) [2](https://old.reddit.com/r/nextdns/comments/xoyyw2/nextdns_as_a_set_it_and_forget_it_solution/iq1k6tx/) [3](https://old.reddit.com/r/nextdns/comments/vuon2a/one_profile_for_lan_devices_another_profile_for/iffegc5/?context=2) [4](https://old.reddit.com/r/nextdns/comments/vn8olr/please_could_someone_recommend_me_a_good/ie5meel/?context=2)  </sup>

### Native Tracking Protection <sup><sup>[1](https://github.com/nextdns/metadata/tree/master/privacy/native)</sup></sup>

Add all the device brands that you use. There's no advantage in adding brands you don't have; however, there’s no disadvantage in adding unused brands, either.

	Xiaomi
	Huawei
	Samsung
	Amazon Alexa
	Windows
	Apple
	Roku
	Sonos

### Block Disguised Third-Party Trackers <sup><sup>[1](https://github.com/nextdns/cname-cloaking-blocklist/blob/master/domains) [2](https://medium.com/nextdns/cname-cloaking-the-dangerous-disguise-of-third-party-trackers-195205dc522a) [3](https://arxiv.org/pdf/2102.09301.pdf) [4](https://tma.ifip.org/2020/wp-content/uploads/sites/9/2020/06/tma2020-camera-paper66.pdf) </sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Block Disguised Third-Party Trackers

### Allow Affiliate & Tracking Links <sup><sup>[1](https://github.com/nextdns/metadata/blob/master/privacy/affiliate-tracking-domains) [2](https://twitter.com/NextDNS/status/1539229377560461312) </sup></sup>
:bulb: Your IP address will automatically be hidden (via [TCP](https://www.educba.com/what-is-tcp-ip/) [proxying](https://en.wikipedia.org/wiki/Proxy_server#/media/File:Proxy_concept_en.svg)) to preserve your privacy.<p>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Allow Affiliate & Tracking Links

***

# Parental Control :family_man_woman_boy:
### YouTube Restricted Mode
![Disabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/disabled.svg) Enforce YouTube Restricted Mode
### Block Bypass Methods <sup><sup>[1](https://github.com/nextdns/metadata/tree/master/parentalcontrol)</sup></sup>
![Disabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/disabled.svg) Block Bypass Methods

***

# Denylist :no_entry:

Denylist entries block any requests from that source.

***

# Allowlist :white_check_mark: 

Allowlist entries override any blocks.

<details>

### Facebook / Instagram

	graph.facebook.com
	graph.instagram.com
	i.instagram.com

### Apple device updates <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/536)</sup></sup> / Apple Music <sup><sup>[2](https://old.reddit.com/r/nextdns/comments/vz9kla/at_last_nextdns_added_the_1host_xtra/ig8zsnn/)</sup></sup> 

	xp.apple.com
	
### Apple iMessage GIFs <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/560)</sup></sup> / Spotlight Search <sup><sup>[2](https://github.com/badmojr/1Hosts/issues/562)</sup></sup> 

	smoot.apple.com
	
### Zoom <sup><sup>[1](https://oisd.nl/excludes.php?w=log.zoom.us) [2](https://oisd.nl/excludes.php?w=us04logfiles.zoom.us)</sup></sup> 

	logfiles.zoom.us
	us04logfiles.zoom.us
	us04zpns.zoom.us

### Epic Games Launcher <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/643)</sup></sup>

	eulatracking-public-service-prod06.ol.epicgames.com

### NVIDIA Gefore Experience <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/650)</sup></sup>
	
	gfe.nvidia.com
	nvgs.nvidia.cn

### [imgur](https://imgur.com/) <sup><sup>[1](https://github.com/lightswitch05/hosts/issues/358)</sup></sup>

	js.media-lab.ai

### [Spectrum](https://www.spectrum.net) login <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/640)</sup></sup>

	pov.spectrum.net

### [CBS](https://www.cbsnews.com/live/#x) News livestream <sup><sup>[1](https://github.com/nextdns/metadata/issues/1030)</sup></sup> 

	production-cmp.isgprivacy.cbsi.com

### [FiveThirtyEight](https://fivethirtyeight.com/) videos / National Geographic website

	dcf.espn.com

### [Men's Health](https://www.menshealth.com/nutrition/a40868905/chris-hemsworth-chicken-pasta-bake-recipe-centr/) videos <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/651)</sup></sup>

	glimmer.hearstapps.com

</details>	

***

# Settings :gear:
### Block Page
![Disabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/disabled.svg) Enable Block Page → :warning: *Enabling may cause breakage if the [NextDNS Root CA](https://help.nextdns.io/t/g9hmv0a/how-to-install-and-trust-nextdns-root-ca) is not on your devices*
### Anonymized EDNS Client Subnet <sup><sup>[1](https://help.nextdns.io/t/m1hmv04/what-is-edns-client-subnet-ecs) </sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Anonymized EDNS Client Subnet
### Cache Boost <sup><sup>[1](https://old.reddit.com/r/nextdns/comments/girmcf/new_setting_cache_boost/)</sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Cache Boost
### CNAME Flattening <sup><sup>[1](https://medium.com/nextdns/nextdns-added-cname-uncloaking-support-becomes-the-first-cross-platform-solution-to-the-problem-e3f437f84342) [2](https://developers.cloudflare.com/dns/additional-options/cname-flattening) [3](https://advancedweb.hu/what-is-cname-flattening-and-how-it-helps-redirecting-the-apex-domain/) </sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable CNAME Flattening
### Web3 <sup><sup> [1](https://twitter.com/NextDNS/status/1491034351391305731) [2](https://gabygoldberg.notion.site/f7050e62461143d49345e7b46eb5576b)</sup></sup>
![Disabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/disabled.svg) Enable Web3
<br>
<br> (optional)

***
# FAQ :question:
### How do I signup for NextDNS?
Click [here](https://nextdns.io/?from=xujj63g5)!

### Do I still need an adblocker with NextDNS?
Yes. <sup>[1](https://help.nextdns.io/t/x2hzbps/using-nextdns-why-is-ublock-origin-still-catching-lots-of-ads) [2](https://github.com/gorhill/uBlock/wiki/About-%22Why-uBlock-Origin-works-so-much-better-than-Pi%E2%80%91hole-does%3F%22) [3](https://old.reddit.com/r/nextdns/comments/t8qn8c/comment/hzqrrfa/?context=3)</sup>

***

# Mentions :books:
Here: [1](https://old.reddit.com/r/moddedandroidapps/comments/wbud1e/aerowitter_twifucker_non_root_twitter_mod/iiloq0p/?context=2) [2](https://old.reddit.com/r/nextdns/comments/xoyyw2/nextdns_as_a_set_it_and_forget_it_solution/?context=3)

***

<div align='center'><a href='https://www.websitecounterfree.com'><img src='https://www.websitecounterfree.com/c.php?d=9&id=19651&s=1' border='0' alt='Free Website Counter'></a><br / ></div>
<div align='center'>23 July 2022</div>


