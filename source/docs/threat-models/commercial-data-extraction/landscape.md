# Faster than the rules

The field has reorganised itself two or three times in a handful of years. Each
reorganisation arrived wearing the language of privacy, and each left collection intact
or larger than before. The pattern underneath is steady: the plumbing changes, the tap
keeps running, and the rules arrive a step behind the pipe they were written for.

## Real-time bidding: collection as broadcast

Selling a single advertising slot works by auction, and the auction is loud. A request
describing the reader, the page open, a rough location, the device, a bundle of inferred
interests, is broadcast to many bidding firms at once so they can price the impression.
Every firm on the list receives that description. Winning the auction is not a condition
of receiving it; losing bidders keep their copy too.

That is why the practice has been called adtech's biggest data breach. The Irish Council
for Civil Liberties, examining the ecosystem in 2022, found Google alone permitted 4,698
companies to receive real-time bidding data about people in the US. There is
no recall. Once a page view has been broadcast, the reader cannot know who holds it, and
neither, in practice, can the firm that sent it.

## The cookie that would not die

For most of a decade the industry prepared for the end of the third-party cookie. Google
announced Chrome would phase it out, and the trade press treated a post-cookie world as
settled. It did not arrive. Google abandoned the deprecation plan in July 2024, dropped
even the promised consent prompt in April 2025, and in October 2025
[retired the Privacy Sandbox technologies](https://privacysandbox.google.com/blog/update-on-plans-for-privacy-sandbox-technologies)
that were meant to replace tracking cookies with something gentler. The third-party cookie
is still there.

The awkward part is what the industry built while waiting. Hashed-email identity graphs
that match a person across sites through their logged-in address, server-side tagging that
moves collection off the browser and onto the advertiser's own machines, tracking
relabelled as first-party to survive browser defences: these were deployed in
anticipation and did not roll back when the deadline evaporated. So collection now runs
on two rails at once. The invasive interim workaround outlived the privacy-preserving
replacement it was supposed to bridge to.

## The SDK economy

Much of the collection on a phone is not done by the apps a person chose. It is done by
third-party code bundled inside them: analytics, advertising, attribution, and location
kits dropped in by the developer, each shipping data back to a firm the user never picked.
A weather app, a torch, a free game, a period tracker may each carry several. The
permission a person grants the app becomes data for its partners, and none of those
partners appear on the store listing. This is one of the main streams feeding the broker
market, since location gathered by an SDK inside an ordinary app can be sold on with the
provenance stripped.

## Consent as theatre

The legal cover for the harvest is consent, and the banner is where consent is
manufactured. The design does the persuading: accept is one bright click, refuse is
several muted ones or buried in a paragraph. The privacy group noyb has filed more than
700 complaints against banners since 2021, and the European Data Protection Board's cookie
banner taskforce set out the catalogue of tricks in its
[January 2023 report](https://www.edpb.europa.eu/our-work-tools/our-documents/other/report-work-undertaken-cookie-banner-taskforce_en):
no reject-all option on the first layer, deceptive button colours, the refusal hidden in
text. The shared standard for recording all this consent has itself been found unlawful.
Enforcement runs case by case and slowly, so the pattern persists while each individual
banner is litigated.

## Inference gets cheaper

The sharpest shift is the quietest. Machine learning lets thinner inputs yield firmer
guesses, so a sensitive trait no longer has to be collected to be known. Health, a
pregnancy, sexuality, financial strain, a political leaning: each can be inferred from
purchase timing, app use, or who a person is connected to, without any of it being
disclosed. This sits awkwardly with rules that restrict collecting sensitive categories,
because nothing sensitive was collected. It was calculated. The profile learns things the
person never entered and, often, never suspected were legible.

## The rules that have started to bite

The counter-pressure is real, though it aims at the mechanics rather than at collection
itself. Since the Digital Services Act took full effect in 2024, platforms may not target
advertising to [minors](../minors/index.rst), nor target anyone using the special
categories of data the GDPR protects. The Digital Markets Act bars the designated
gatekeepers from combining a person's data across their own services for advertising
without consent. Both bite on how the profile is used and joined up. Neither stops the
profile being built.

Meanwhile the law written for the cookie itself has stalled. The ePrivacy Regulation,
proposed in 2017 to modernise the rules the banners rest on, has still not been adopted.
The mechanics keep moving; the instrument meant to govern them sits unfinished.

## What has actually changed

Three shifts explain why the terrain feels different. Collection moved off the browser and
onto servers and identity graphs, so browser defences reach less of it than they did.
Sensitive attributes shifted from collected to inferred, slipping the rules that assume
collection is the risky step. And regulation turned to the mechanics, consent, combination,
sensitive categories, minors, which leaves the building of the profile largely untouched.

Underneath the language of each rearrangement, collection has not shrunk. It changed rails.

Last reviewed: 2026-07-16.
