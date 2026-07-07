# From fingerprint to name

Browser fingerprinting identifies a device with no cookie, no login and no consent, by the unique combination of its
technical traits. For years the open question was whether anyone actually used it to track people, and whether it could
be joined to a real identity. Both are now answered.

## What the research shows

A browser fingerprint is built from a device's configuration: its GPU and how it renders graphics, its fonts, screen
resolution, audio hardware, timezone and language. The combination is distinctive enough that foundational research
measured over 90% uniqueness across devices. In 2025 researchers at Texas A&M and Johns Hopkins
published [FPTrace](https://engineering.tamu.edu/news/2025/06/websites-are-tracking-you-via-browser-fingerprinting.html), a
framework that inferred, from how ad systems behaved when a fingerprint changed, that websites are in fact using
fingerprinting to track users across sessions and sites, persisting after cookies are cleared, and feeding those
profiles into real-time advertising bids. As one of the researchers put it, until then there had been no hard proof that
fingerprinting was actually being used to track people; opting out under the GDPR did not stop it.

Separate 2025 disclosures showed [Meta and Yandex making the link to identity directly](https://arstechnica.com/security/2025/06/meta-and-yandex-are-de-anonymizing-android-users-web-browsing-identifiers/):
tracking scripts embedded in millions of websites passed browser identifiers over localhost to the Facebook,
Instagram and Yandex apps on the same Android device, where the logged-in account tied the "anonymous" browsing
to a named person, private browsing included.

## Why it counts

Fingerprinting is the identifier that survives the standard defences. Clearing cookies, private-browsing mode and
consent refusals do not remove it, because it is not stored on the device; it is recomputed from the device each time.
That makes it a [device-fingerprint asset](../assets.md) the
ordinary [tracker-blocking advice](../../../playbooks/blocks.md) only partly addresses, and a direct feed into
the [commercial data layer](../../surveillance/cases/databroker-files.md) that the surveillance model shows reaching all
the way to named officials.
