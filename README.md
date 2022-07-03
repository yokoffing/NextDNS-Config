***

# Security
### Threat Intelligence Feeds
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Use Threat Intelligence Feeds
### AI-Driven Threat Detection
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable AI-Driven Threat Detection
### Google Safe Browsing
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Google Safe Browsing
### Cryptojacking Protection
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Cryptojacking Protection → :radioactive: *Enabling may cause breakage (unlikely)*
### DNS Rebinding Protection
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg)  Enable DNS Rebinding Protection → :radioactive: *Enabling may cause breakage (unlikely)*
### IDN Homograph Attacks Protection
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Homograph Attacks Protection
### Typosquatting Protection
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Typosquatting Protection
### Domain Generation Algorithms (DGAs) Protection
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable DGA Protection
### Block Newly Registered Domains (NRDs)
![Disabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/disabled.svg) Block Newly Registered Domains (NRDs) → :radioactive: *Enabling may cause breakage*
### Block Dynamic DNS Hostnames
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Block Dynamic DNS Hostnames
### Block Parked Domains
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Block Parked Domains

### Block Top-Level Domains (TLDs)
```
agency
asia
bar
bid
buzz
cam
casa
cf
club
cn (optional)
cricket
date
email
fail
fit
fun
ga
gdn
ge
gq
guru
help
host
icu
info
ir
link
live
loan
ltda
men
ml
nagoya
nf
okinawa
online
ooo
press
pw
recipes
rest
review
rodeo
ryukyu
shop
site
space
su
support
surf
tk
tokyo
top
ug
vip
wang
webcam
website
win
work
ws
```

Intentional Exceptions:
```
biz
cc
life
monster
pro
ru
xyz
```

### Block Child Sexual Abuse Material
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Block Child Sexual Abuse Material

***

# Privacy
### Blocklists
There seems to be a lot of activity on [Github](https://github.com/badmojr/1Hosts/commits/master?before=fb857882973986a3ac4575cd1d79d9079d363866+35&branch=master&qualified_name=refs%2Fheads%2Fmaster) and [Reddit](https://www.reddit.com/user/badmojr/comments/) in the past months to remove breakage from 1Hosts **Pro** (see [this](https://www.reddit.com/r/nextdns/comments/uxwabr/kind_of_amazed_at_1hosts_pro/ia2gyta/?context=3) and [that](https://www.reddit.com/r/nextdns/comments/v6yiqe/what_filterlists_do_you_recommend/ic51pa8/?context=3)). But if you experience significant breakage due to this list, drop down to 1Hosts **Lite**.

	NextDNS Ads & Trackers Blocklist
	AdGuard DNS filter
	oisd
	1Hosts (Pro)
### Native Tracking Protection
:radioactive: *Enabling may cause breakage (unlikely)*

Add these brands according to what devices you use; there is no advantage to adding brands you don't own. However, there’s *not* a strong reason to omit any brands either.

	Xiaomi
	Huawei
	Samsung
	Amazon Alexa
	Windows
	Apple
	Roku
	Sonos
### Block Disguised Third-Party Trackers
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Block Disguised Third-Party Trackers
### Allow Affiliate & Tracking Links
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Allow Affiliate & Tracking Links

***

# Parental Control
### YouTube Restricted Mode
![Disabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/disabled.svg) Enforce YouTube Restricted Mode → :radioactive: *Enabling may cause breakage*

### Block Bypass Methods
![Disabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/disabled.svg) Block Bypass Methods → :radioactive: *Enabling may cause breakage*

***

# Denylist
(optional) Most of these are blocked under [Block Dynamic DNS Hostnames](https://github.com/yokoffing/NextDNS-Config/edit/main/README.md#block-dynamic-dns-hostnames) (see [here](https://github.com/nextdns/metadata/blob/master/security/ddns/suffixes)).

	pubnub.com
	ddns.net
	duckdns.org
	hopto.org
	linkpc.net
	myddns.me
	myftp.biz
	myftp.org
	ngrok.io
	no-ip.biz
	no-ip.org
	portmap.host
	portmap.io
	publicvm.com
	sytes.net
	zapto.org

***

# Allowlist
if using Facebook and Instagram:

	graph.facebook.com
	graph.instagram.com

breaks CBS News (NextDNS Ads & Trackers Blocklist):

	production-cmp.isgprivacy.cbsi.com
***

# Settings
### Block Page
![Disabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/disabled.svg) Enable Block Page → :radioactive: *Enabling may cause breakage if the NextDNS Root CA is not on your devices*
### Anonymized EDNS Client Subnet
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Anonymized EDNS Client Subnet
### Cache Boost
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable Cache Boost
### CNAME Flattening
![Enabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/enabled.svg) Enable CNAME Flattening
### Web3 (optional)
![Disabled](https://raw.githubusercontent.com/crssi/NextDNS-Config/main/icons/disabled.svg) Enable Web3

***

# Credit
Forked from the [crssi](https://github.com/crssi/NextDNS-Config#readme) config. Some inputs came from the [scafroglia93](https://github.com/scafroglia93/nextdns-setting]) config while other changes are my own.

***
