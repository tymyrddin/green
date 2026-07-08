# Switching to a privacy-focused browser

## Alternatives to Chrome

Firefox, with privacy settings: blocks trackers by default, supports extensions such as uBlock Origin, and has a Strict tracking-protection mode in settings.

Brave: ships with an ad and tracker blocker, can route private tabs through Tor, and offers an optional scheme that pays in cryptocurrency for viewing privacy-respecting ads.

Tor Browser: the most private of the three, routing traffic through several relays and resisting fingerprinting by design. It is slower, which suits sensitive browsing rather than everyday use.

## Hardening the browser

Chrome can be tightened without switching, though it starts from a weaker position:

* Block third-party cookies at `chrome://settings/cookies`
* [Disable Chrome's Topics API](../runbooks/disable-chrome-topics.md)
* [Install Privacy Badger to block hidden trackers](blocks.md)
* [Use a VPN to hide the IP address](vpn.md)

Last reviewed: 2026-07-08.
