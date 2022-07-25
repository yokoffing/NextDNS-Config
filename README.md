***
# Guidelines
1) Must pass the "[girlfriend test](https://www.urbandictionary.com/define.php?term=Grandma%20Test)".
2) Follow the [law of diminishing returns](https://pmctraining.com/site/wp-content/uploads/2018/04/Law-of-Diminishing-Returns-CHART.png) by not overblocking (e.g., using [Energized Ultimate](https://old.reddit.com/r/nextdns/comments/v0wwjf/does_energized_ultimate_blocklist_contain/iak0a79/) or [1Hosts Xtra](https://old.reddit.com/r/nextdns/comments/vz9kla/at_last_nextdns_added_the_1host_xtra/ig7fkia/?context=3), blocking too many [TLDs](https://github.com/yokoffing/NextDNS-Config#block-top-level-domains-tlds), etc.).

***

# Security
### Threat Intelligence Feeds <sup><sup>[1](https://github.com/nextdns/metadata/blob/master/security/threat-intelligence-feeds.json)</sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Use Threat Intelligence Feeds
### AI-Driven Threat Detection
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable AI-Driven Threat Detection
### Google Safe Browsing <sup><sup> [1](https://safebrowsing.google.com/safebrowsing/report_general/) [2](https://user-images.githubusercontent.com/11689349/107696360-d8dde800-6c7f-11eb-9882-cccc8d2065c5.jpg) [3](https://the8-bit.com/apple-proxies-google-safe-browsing-privacy/) [4](https://github.com/brave/brave-browser/wiki/Deviations-from-Chromium-(features-we-disable-or-remove)#services-we-proxy-through-brave-servers) </sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Google Safe Browsing
### Cryptojacking Protection <sup><sup>[1](https://github.com/nextdns/metadata/blob/master/security/cryptojacking.json)</sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Cryptojacking Protection
### DNS Rebinding Protection <sup><sup>[1](https://help.nextdns.io/t/35hmval/what-is-dns-rebinding-protection)</sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg)  Enable DNS Rebinding Protection → :radioactive: *Enabling may cause breakage (unlikely)*
### IDN Homograph Attacks Protection
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Homograph Attacks Protection
### Typosquatting Protection <sup><sup>[1](https://github.com/nextdns/metadata/blob/master/security/typosquatting/protected-domains)</sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Typosquatting Protection
### Domain Generation Algorithms (DGAs) Protection
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable DGA Protection
### Block Newly Registered Domains (NRDs) <sup><sup>[1](https://www.malwarebytes.com/glossary/phishing) [2](https://old.reddit.com/r/uBlockOrigin/comments/w64sqt/comment/ihboutk/?context=3) [3](https://www.boldgrid.com/instagram-influencer-accounts-are-being-hacked-phishing-attacks/) </sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Block Newly Registered Domains (NRDs) → :radioactive: *Enabling may cause breakage*
<br>
<br>Blocking NRDs will cause false positives [occasionally](https://old.reddit.com/r/InternetIsBeautiful/comments/w2wdro/comment/iguvg8y/?context=3); however, if you are comfortable allowlisting, it is **strongly encouraged** that you enable this. Add NRDs to your allowlist selectively; and if you do, **NEVER** give sensitive information to a NRD.
### Block Dynamic DNS Hostnames <sup><sup>[1](https://github.com/nextdns/metadata/blob/master/security/ddns/suffixes) [2](https://twitter.com/NextDNS/status/1541740963760144386?cxt=HHwWhIC8iZ7PruUqAAAA) [3](https://www.phishing.org/what-is-phishing) </sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Block Dynamic DNS Hostnames
### Block Parked Domains <sup><sup>[1](https://github.com/nextdns/metadata/blob/master/security/parked-domains-cname)</sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Block Parked Domains
### Block Top-Level Domains (TLDs) <sup><sup>[1](https://www.gomyitguy.com/blog-news-updates/malicious-domain-extensions) [2](https://www.spamhaus.org/statistics/tlds/) [3](https://thrivemyway.com/info-websites/) [4](https://www.bleepingcomputer.com/news/security/verified-twitter-accounts-hacked-to-send-fake-suspension-notices/)</sup>
:radioactive: *Enabling may cause breakage*

```
.work
.fit
.surf
.info
.cam
.ci
.cf
.cn
.ga
.gq
.ml
.online
.tk
.top
```

### Block Child Sexual Abuse Material
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Block Child Sexual Abuse Material

***

# Privacy
### Blocklists <sup><sup>[1](https://github.com/nextdns/metadata/tree/master/privacy/blocklists)</sup>

Use **1Hosts (Lite)** instead of **1Hosts (Pro)** if you do not [report](https://github.com/badmojr/1Hosts/issues) false positives and add to the allowlist.

	NextDNS Ads & Trackers Blocklist
	oisd
	1Hosts (Pro)

	
### Native Tracking Protection <sup><sup>[1](https://github.com/nextdns/metadata/tree/master/privacy/native)</sup>
:radioactive: *Enabling may cause breakage (unlikely)*

Add these brands according to what devices you use. There's no advantage in adding brands you don't own; however, there’s no disadvantage in adding unused brands either.

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
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Allow Affiliate & Tracking Links

***

# Parental Control
### YouTube Restricted Mode
![Disabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/disabled.svg) Enforce YouTube Restricted Mode → :radioactive: *Enabling may cause breakage*
### Block Bypass Methods <sup><sup>[1](https://github.com/nextdns/metadata/tree/master/parentalcontrol)</sup>
![Disabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/disabled.svg) Block Bypass Methods → :radioactive: *Enabling may cause breakage*

***

# Denylist

	N/A

***

# Allowlist
### Facebook

	graph.facebook.com

### Apple device updates <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/536)</sup> </sup> / Apple Music <sup><sup>[2](https://old.reddit.com/r/nextdns/comments/vz9kla/at_last_nextdns_added_the_1host_xtra/ig8zsnn/)</sup></sup> 

	xp.apple.com
	
### Apple iMessage GIFs <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/560)</sup></sup> / Spotlight Search <sup><sup>[2](https://github.com/badmojr/1Hosts/issues/562)</sup></sup> 

	smoot.apple.com
	
### Zoom <sup><sup>[1](https://oisd.nl/excludes.php?w=log.zoom.us) [2](https://oisd.nl/excludes.php?w=us04logfiles.zoom.us)</sup></sup> 
Zoom untrusted certificate error messages when [Block Page](https://github.com/yokoffing/NextDNS-Config#block-page) is enabled.

	logfiles.zoom.us
	us04logfiles.zoom.us
	us04zpns.zoom.us

### [CBS](https://www.cbsnews.com/live/#x) News livestream <sup><sup>[1](https://github.com/nextdns/metadata/issues/1030)</sup></sup> 

	production-cmp.isgprivacy.cbsi.com

### Microsoft Office 365 <sup><sup>[1](https://github.com/badmojr/1Hosts/issues/565) [2](https://oisd.nl/excludes.php?w=mobile.pipe.aria.microsoft.com)</sup></sup> 
Disclaimer: You may only want to allowlist these requests if you're using the file collaboration features.

	self.events.data.microsoft.com
	mobile.pipe.aria.microsoft.com

### Xbox Live achievements <sup><sup>[1](https://github.com/lightswitch05/hosts/issues/161#issuecomment-614973289) [2](https://discourse.pi-hole.net/t/commonly-whitelisted-domains/212#xbox-live-18)</sup></sup>  / Microsoft "Your Phone" <sup><sup>[3](https://github.com/lightswitch05/hosts/issues/161#issuecomment-838590100)</sup></sup> 
Disclaimer: I don't use these, so I can't confirm these entries.

	v10.events.data.microsoft.com
	v20.events.data.microsoft.com

***

# Settings
### Block Page
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Block Page → :radioactive: *Enabling may cause breakage if the [NextDNS Root CA](https://help.nextdns.io/t/g9hmv0a/how-to-install-and-trust-nextdns-root-ca) is not on your devices*
### Anonymized EDNS Client Subnet <sup><sup>[1](https://help.nextdns.io/t/m1hmv04/what-is-edns-client-subnet-ecs) </sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Anonymized EDNS Client Subnet
### Cache Boost
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Cache Boost
### CNAME Flattening <sup><sup>[1](https://medium.com/nextdns/nextdns-added-cname-uncloaking-support-becomes-the-first-cross-platform-solution-to-the-problem-e3f437f84342) [2](https://developers.cloudflare.com/dns/additional-options/cname-flattening) [3](https://advancedweb.hu/what-is-cname-flattening-and-how-it-helps-redirecting-the-apex-domain/) </sup></sup>
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable CNAME Flattening
### Web3 <sup><sup> [1](https://twitter.com/NextDNS/status/1491034351391305731) </sup> </sup>
![Disabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/disabled.svg) Enable Web3
<br>
<br> (optional)

***

# Credit
Forked from the [crssi](https://github.com/crssi/NextDNS-Config#readme) config. Some inspiration came from the [scafroglia93](https://github.com/scafroglia93/nextdns-setting/blob/master/nextdns-setting.txt) config while other ideas are my own.

***

<div align='center'><a href='https://www.websitecounterfree.com'><img src='https://www.websitecounterfree.com/c.php?d=9&id=19651&s=1' border='0' alt='Free Website Counter'></a><br / ></div>
<div align='center'>23 July 2022</div>


