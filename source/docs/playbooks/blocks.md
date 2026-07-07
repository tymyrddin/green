# Blocking tracking scripts

Most websites carry hidden trackers that watch browsing habits, build profiles, and slow pages down. Two free extensions, uBlock Origin and Privacy Badger, block the bulk of them and are the least demanding place to start.

## What tracking scripts do

Tracking scripts are small pieces of code that:

* Record which sites a browser visits, including in private mode
* Slow browsing by loading extra ads and trackers
* Build a profile that is sold to advertisers and data brokers

Common examples include Google Analytics (present on a large share of sites), the Facebook Pixel (tracks visitors for targeted ads), and real-time bidding scripts from the ad-tech industry.

## uBlock Origin

uBlock Origin blocks ads, trackers and malware domains, stays current through filter lists such as EasyList, and stays light on browser resources. It installs from the extension store for Chrome, Edge, Brave and Firefox, with limited support on Safari.

The extra filter lists are worth enabling. Open the uBlock icon, then Dashboard, then the Filter lists tab, and enable:

* EasyPrivacy (blocks trackers)
* uBlock filters, Annoyances (suppresses cookie pop-ups)
* AdGuard Tracking Protection

When a blocked element breaks a page, the element zapper (the uBlock icon, then the zapper tool) removes a single element by hovering and clicking it.

## Privacy Badger

Privacy Badger learns and blocks trackers as browsing happens, with no manual lists, and stops third-party cookies from following between sites. It runs alongside uBlock Origin. It comes from the EFF's official site for Chrome, Firefox and Edge, works without setup, and shows what it has blocked from its toolbar icon.

## Stricter blocking

For tighter control, uBlock Origin's Dashboard, under My filters, accepts dynamic rules that block all third-party content and scripts:

```
* * 3p block
* * 3p-script block
```

This breaks some sites but stops nearly all tracking. Firefox Multi-Account Containers isolate logins, keeping Facebook in one container and Google in another. NextDNS or Pi-hole block trackers for every device on a network at once.

## What these tools miss

* Browser fingerprinting, which Firefox's `resistFingerprinting` setting addresses
* IP-level tracking, which a trusted VPN such as ProtonVPN or Mullvad covers
* First-party tracking, such as a retailer watching clicks on its own site

For most people, uBlock Origin and Privacy Badger together are enough to set and forget. A stricter setup pairs uBlock in hard mode with Firefox Containers and NextDNS. Neither makes a browser anonymous, but both stop most tracking and tend to speed pages up.

## Testing

* [Cover Your Tracks (EFF)](https://coveryourtracks.eff.org/)
* [WhoTracks.Me](https://whotracks.me/)
