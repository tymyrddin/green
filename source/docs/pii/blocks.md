# How to block tracking scripts with uBlock Origin and Privacy Badger

Modern websites are filled with hidden trackers that monitor your browsing habits, build profiles about you, 
and slow down page loading. The easiest way to stop this is by using uBlock Origin and Privacy Badger—two powerful 
(and free) tools that block invasive tracking scripts.

## Why block tracking scripts?

Tracking scripts are bits of code that:

* Record every site you visit (even in private mode)
* Slow down your browsing (by loading unnecessary ads/trackers)
* Build a profile about you (sold to advertisers and data brokers)

Common trackers include:

* Google Analytics (embedded in ~50% of all websites)
* Facebook Pixel (tracks visitors for targeted ads)
* AdTech scripts (real-time bidding networks)

## uBlock Origin: The best blocker

What it does:

* Blocks ads, trackers, and malware domains
* Uses filter lists (like EasyList) to stay updated
* Lightweight (unlike some ad blockers, it doesn’t slow your browser)

Install from your browser’s extension store

* Chrome/Edge/Brave
* Firefox
* Safari (limited)

Enable Extra Filter Lists (Recommended) by clicking the uBlock icon → ⚙️ Dashboard → "Filter lists" tab

Check:

* EasyPrivacy (blocks trackers)
* uBlock filters – Annoyances (stops cookie pop-ups)
* AdGuard Tracking Protection

Use "Zapper" mode for sneaky trackers: If a site breaks (due to blocking), click the uBlock icon → 🚫 "Zapper" → hover 
over the broken element → click to remove it.

## Privacy Badger: Automatic tracker blocking

What it does

* Learns and blocks trackers as you browse (no manual lists needed)
* Stops third-party cookies from following you
* Works alongside uBlock Origin

How to install & use

* Get it from EFF’s official site (Chrome/Firefox/Edge)
* It works automatically—no setup needed!
* Check blocked trackers by clicking its icon in the toolbar.

## Hard mode (maximum blocking)

For even stricter privacy, use 

***uBlock Origin Settings***: Go to Dashboard → "My filters" → Add:

```
* * 3p block
* * 3p-script block
```

This breaks some sites but blocks nearly all tracking.

***Firefox + Multi-Account containers*** isolates logins (e.g., Facebook in one container, Google in another)

***NextDNS / Pi-hole*** Blocks trackers at the network level (for all devices)

## What these tools do not block

* Browser fingerprinting (use Firefox with resistFingerprinting enabled)
* VPN/IP tracking (use a trusted VPN like ProtonVPN or Mullvad)
* First-party tracking (e.g., Amazon watching what you click)

## Recommendation

* For most people: uBlock Origin + Privacy Badger (set and forget)
* For advanced users: uBlock (hard mode) + Firefox Containers + NextDNS

These tools won’t make you 100% anonymous, but they’ll stop most tracking and speed up your browsing.