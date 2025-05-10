# How (and why) to reset your advertising ID regularly

Your smartphone’s advertising ID is a unique tracker assigned to your device that allows companies to build a 
profile of your app usage, interests, and behaviour—even if you don’t log in anywhere. Here’s how to reset it on 
Android and iOS to disrupt tracking.

## What is an advertising ID?

An advertising ID lets apps and ad networks link your activity across different services to target ads.

* Android: Called the "Google Advertising ID" (GAID)
* iOS: Called the "Identifier for Advertisers" (IDFA)

Example: If you search for "hiking boots" in Chrome, Instagram might show you boot ads later—even if you weren’t logged in.

## Why reset it weekly?

* Breaks tracking chains – Resetting creates a new random ID, making it harder to build a long-term profile.
* Limits personalized ads – You’ll still see ads, but they’ll be less targeted.
* Works even if you don’t opt out – Some apps ignore "Opt out of ads personalization" but still use the ID for analytics.

## How to reset on Android

* Open Settings → Google → Ads
* Tap "Reset advertising ID"
* (Optional) Enable "Opt out of ads personalization" to limit tracking further.

Note: Some Android skins (Samsung, Xiaomi, etc.) bury this setting. Try searching for "advertising ID" in Settings.

## How to reset on iOS

* Open Settings → Privacy & Security → Tracking
* Toggle off "Allow Apps to Request to Track" (blocks IDFA access entirely).
* To reset, Go to Settings → Privacy & Security → Apple Advertising and tap "Reset Advertising Identifier"

## Limitations to know

* Doesn’t stop all tracking – Fingerprinting, IP logging, and first-party data (e.g., Google/Facebook logged-in tracking) still work.
* Some apps bypass it – Especially if you use the same Google/Apple account everywhere.
* Resets aren’t instant – It can take hours for ad networks to update.

## Extra steps for stronger privacy

* Use a firewall app (e.g., TrackerControl for Android) to block hidden trackers.
* Disable personalized ads in Google (adssettings.google.com).
* On iOS, use Lockdown Mode (Settings → Privacy & Security → Lockdown Mode) to cut off most tracking.

## Automate it

* Android: Use Tasker or MacroDroid to reset the ID weekly.
* iOS: Shortcuts app can’t reset the IDFA, but you can set a reminder.

Combine with other anti-tracking tools

## For best results

* Reset advertising ID weekly
* Use Firefox Focus for private browsing
* Block ads/trackers with NextDNS or AdGuard

This won’t make you invisible, but it fragments your data enough to reduce profiling.