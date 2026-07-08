# Protecting reproductive and health data

Health information is some of the most sensitive you hold, and some of the most eagerly collected. Cycle-tracking apps, the location your phone gives off near a clinic or a pharmacy, what you pay for and where, what you search for, and who you message about it all leave a trail, and data brokers make a business of joining those trails together.

In the UK and the EU, health data is treated as a special category under data protection law, which in principle carries extra protection. Protection in law is not the same as protection in practice, though, and the stakes rise sharply if you travel to, or live somewhere, the care you need is restricted or criminalised.

None of this is about doing everything. Pick the parts that fit your situation.

## Cycle and health apps

A period or fertility app holds a detailed record of your body over time. Where that record lives is the question. Many popular apps keep it on their own servers, tied to an account, where it can be shared, sold, or handed over under legal pressure.

The safer pattern is an app that stores everything on your device and nothing in the cloud. [Euki](https://eukiapp.org/) is one such: it keeps data only on the phone, needs no account, is open source, and includes a decoy PIN for a screen you can hand over. Drip and Periodical work on the same local-only principle. Rather than trust any single recommendation, including this one, which will date, Mozilla's [Privacy Not Included](https://www.mozillafoundation.org/en/privacynotincluded/) reviews these apps and is kept current. The question to carry into that comparison is simple: does my data leave the phone, and if so, to whom.

If you would rather not use an app at all, a note on paper reveals nothing to anyone.

## Location

Your phone broadcasts where it is to many of the apps on it, and some of them sell that on. In 2022 it emerged that data brokers had been selling location data that could pick out visits to family-planning clinics, sourced from tracking code buried in ordinary apps. The firms involved pledged to stop once it was reported, but the mechanism, ordinary apps leaking location to brokers, did not go away.

Reducing that exposure is the same work as general location hygiene: turn off the advertising identifier and app tracking (the [advertising ID runbook](../runbooks/adids.md)), and tighten which apps can see your location at all (the [device hardening playbook](device-hardening.md)). Leaving the phone at home, or switched off, before a sensitive appointment removes the signal entirely.

## Payments and purchases

A card payment names the merchant, the time, and the amount. A pharmacy, a clinic, or a subscription shows up in a statement that others on a joint account can see, and that the card issuer retains. Where a purchase is sensitive, cash or a privacy-preserving payment method keeps it off that record. The [payment playbook](payment.md) covers the options.

## Search and browsing

What you look up is revealing, and it is logged by your search engine, your browser, and often your network. A private search engine, a browser that is not signed into a data-hungry account, and the tracker blocking in the [blocking scripts playbook](blocks.md) and the [Chrome hardening playbook](chrome.md) all reduce what is kept. The [minimise playbook](minimise.md) covers cutting down the wider trail.

## Messaging

This is the exposure that has done the most damage in practice. In a 2022 Nebraska case, police obtained a mother and daughter's Facebook Messenger conversations under a warrant and used them as evidence in an abortion-related prosecution. Those messages were not end-to-end encrypted, so the platform could read them and hand them over.

Conversations about health, or about seeking care, are safest on an end-to-end encrypted channel where the provider cannot read them and so cannot be compelled to produce them. The [encrypted messaging playbook](messaging.md) covers moving to Signal, and turning on disappearing messages so that little is left to retrieve later.

## If you are travelling somewhere more hostile

The calculation changes when you cross a border into a jurisdiction where the care you need is criminalised. Data that is merely commercial in one place can become evidence in another. Before travelling, it is worth thinning what the phone carries: the [travel devices playbook](travel-devices.md) covers preparing a device that reveals little if it is searched, and moving sensitive conversations and records off it beforehand.

## Clearing the trail already left

For data that is already out there, UK and EU law gives you rights to see and delete it. The [data subject request runbook](../runbooks/data-subject-request.md) covers asking an organisation what it holds, the [GDPR deletion runbook](../runbooks/gdpr-deletion.md) covers erasure, and the [data broker playbook](brokers.md) covers the brokers specifically, who are the ones most likely to be quietly reselling health-adjacent signals.

Last reviewed: 2026-07-08.
