---
title: "MacOS"
date: 2022-06-09T11:17:12+07:00
description: "Tips for MacOS"
---



## Introduction

This guide will give you an idea how to set up MacOS in the most private way.

## Getting started

Unsync anything you can. Apple loves to track everything from your location to your favorite activities. Apple can pass on your data to big marketing companies willing to buy info for their targetting.
1. App Store > Store > Logout
2. System Preferences > Bluetooth > Turn off.
3. System Preferences > Users & Groups > Guest User > Uncheck all.
4. System Preferences > Apple ID > Uncheck all.
5. System Preferences > Apple ID > Overview > Sign out.
5. Follow the hardening guide in Reference.

### Notes
#### Bluetooth
- Bluetooth is silently enabled each time your Mac is updated. Put the bluetooth logo in the dock as shown in _appendix_ so you can be rest assured it is not turned on.
- Even with Bluetooth disabled, your macos can be 'woken up' remotely through this service. Just the average human won't be able to do so.

## Setting up controls

Our MacOS will by default try to sneak in advertisements, call home (tracking), sent metrics every 15 minutes and make life miserable at our cost of trying to keep our privacy. Customise the recommendations below to your to your need.

### Package manager brew

Copy and paste the following into your terminal

```
xcode-select --install
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

{{% notice note %}}
Installing xcode-select takes a long time (40 minutes)
{{% /notice %}}

### Components and relevant tool choices
| Component | Tool |
| --- | --- |
| Browser | Librewolf |
| Browser Extensions | https://www.privacytools.io/#browser-addons |
| Mail Client | Thunderbird |
| Mail Provider | [Protonmail](https://protonmail.com/) Tutanota |
| Mail Alias | [SimpleLogin](https://simplelogin.io/) |
| Password Manager | Bitwarden |
| 2FA | Authy |
| File encryption / Archive | Keka |
| Text Messenger | Signal |
| VoIP | Jitsi-meet |
| Notes | Joplin |
| Productivity | Libreoffice |
| Anonymising Networks | ?   |
| Torrent | Transmission |
| Metadata Cleaner | Exifcleaner |
| VPN | [Lokinet](https://lokinet.org/) |
| dVPN | [Alliance](https://dvpnalliance.org/) [Sentinel](https://sentinel.co/dvpn/) [Mysterium](https://www.mysteriumvpn.com/) |
| Cloud Storage | Mega |
| Social media | Freetube(Video) [Redact (Cleaner)](https://redact.dev/) |
| DNSSEC + Adblock | [NextDNS](https://nextdns.io/) |


#### 1. Automated installation

```
brew install librewolf thunderbird tutanota bitwarden authy keka jitsi-meet joplin libreoffice exifcleaner megasync freetube
brew install --cask transmission
```

#### 2. Manual installation

- [Browser Extensions](https://github.com/arkenfox/user.js/wiki/4.1-Extensions)[](https://www.privacytools.io/#browser-addons)[](https://github.com/arkenfox/user.js/wiki/4.1-Extensions)
    - User.js: `git clone https://github.com/arkenfox/user.js.git`
    - uBlock Origin Filters:
        - [LegitimateURLShortener](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/LegitimateURLShortener.txt)
        - [Clear\_urls\_uboified](https://raw.githubusercontent.com/DandelionSprout/adfilt/master/ClearURLs%20for%20uBo/clear_urls_uboified.txt)
- SimpleLogin: https://simplelogin.io/
- ProtonMail: https://protonmail.com/
- NextDNS: https://nextdns.io/
- Redact: https://redact.dev/download

## References
- [Hardening MacOS](https://www.bejarano.io/hardening-macos/)
- [Disable bluetooth](https://www.computerhope.com/issues/ch002099.htm)
- [Dr Duh's Privacy Guide](https://github.com/drduh/macOS-Security-and-Privacy-Guide)
- [Mad Aidan's Guide](https://madaidans-insecurities.github.io/security-privacy-advice.html#browser)

## Appendix
![App Store](/static/app_store_logout.png)