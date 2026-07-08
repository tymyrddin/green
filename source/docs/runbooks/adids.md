# Resetting the advertising ID

A smartphone's advertising ID is a unique tracker assigned to the device. It lets companies build a profile of app usage, interests and behaviour without anyone logging in anywhere. Resetting it regularly disrupts that profile.

## The advertising ID

An advertising ID lets apps and ad networks link activity across services to target ads.

* Android: the Google Advertising ID (GAID)
* iOS: the Identifier for Advertisers (IDFA)

A search for "hiking boots" in one app can surface boot ads in another later, with no login involved, because both saw the same ID.

## The gain from a reset

* Resetting mints a new random ID, which breaks the chain that builds a long-term profile.
* Ads still appear, but with less targeting.
* It helps even without opting out, since some apps ignore the "opt out of ads personalisation" setting but still use the ID for analytics.

## On Android

* Open Settings, Google, Ads
* Tap Reset advertising ID
* Optionally enable "Opt out of ads personalisation" to limit tracking further

Some Android skins (Samsung, Xiaomi) bury this setting; searching Settings for "advertising ID" finds it.

## On iOS

* Open Settings, Privacy and Security, Tracking
* Turn off "Allow Apps to Request to Track", which blocks IDFA access entirely
* Current iOS has no separate reset button (it was removed in iOS 14); with tracking turned off the IDFA is replaced by zeros, which achieves the same thing

## Limitations

* It does not stop all tracking; fingerprinting, IP logging and first-party data (logged-in tracking by Google or Facebook) still work.
* Some apps bypass it, especially when the same Google or Apple account is used everywhere.
* Resets are not instant; ad networks can take hours to update.

## Stronger measures

* A firewall app such as TrackerControl for Android blocks hidden trackers.
* Google's own ad personalisation can be disabled at adssettings.google.com.
* On iOS, Lockdown Mode (Settings, Privacy and Security, Lockdown Mode) hardens the device against targeted spyware; it is aimed at that threat rather than at everyday ad tracking.

## Automating it

* On Android, Tasker or MacroDroid can reset the ID weekly.
* On iOS, the Shortcuts app cannot reset the IDFA, but a weekly reminder covers it.

A weekly reset, paired with Firefox Focus for private browsing and NextDNS or AdGuard for ad and tracker blocking, fragments the data enough to reduce profiling. It does not confer invisibility.

## Testing

* [Exodus Privacy: Android app tracker reports](https://reports.exodus-privacy.eu.org/)
* [Lockdown Privacy (iOS)](https://lockdownprivacy.com/)
