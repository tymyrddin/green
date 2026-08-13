# Switching off beats blocking

Location reaches the broker market by three routes, and a firewall touches one of them. An app with location permission
sends coordinates to its own servers, which looks identical to the app working. An advertising kit inside the app sends
them to a tracker, which is the route a blocker can cut. And an address seen by any service gives a rough position
without asking anyone's permission. Picking a tool is mostly a matter of knowing which route you are closing.

## Do these first, whatever you install

The guide netzpolitik.org published out of its own broker investigation, the
[seven ways](../runbooks/location-brokers.md), opens with the identifier and the app permissions. A blocker appears
fourth, and only for the address.

* Turn the [advertising identifier](../runbooks/adids.md) off, or zero it. It is the join key that lets one app's
  coordinates be matched to another's. A blocked tracker on a phone that still broadcasts a stable identifier is a
  smaller win than it looks.
* Deny precise location to everything that does not visibly need it, and prefer approximate where the option exists. A
  weather app will take a typed-in city. This closes collection at the source, which no network tool can do.
* Remove the two or three apps doing the most of it. Games, dating, weather, shopping and news apps are the categories
  the broker files were full of, and uninstalling one is more effective than filtering it forever.

## Nobody publishes the list

No maintained register of apps that sell location exists, and the closest thing to one was withheld on purpose. The
journalists holding the file naming some 40,000 apps
[published only a few of them](https://netzpolitik.org/2025/databroker-files-neuer-datensatz-enthuellt-40-000-apps-hinter-standort-tracking/),
the ones they could examine and put to the providers for comment, and said the full list "könnte falsche Schlüsse
nahelegen", could invite false conclusions, because the problem is structural rather than particular to an app.
Absence from a one-day sample is chance rather than a clean bill, and a flat list would erase the difference between an
app with coarse location derived from an address and one accurate to the metre. The records in these files come out of
real-time bidding, so any app carrying advertising is a candidate source, which is the other thing a list of names
would hide.

What is maintained catalogues capability rather than sale. [Exodus Privacy](https://reports.exodus-privacy.eu.org/en/)
analyses Android apps for embedded trackers, statically, without decompiling them, and its reports list what is inside
an app rather than what an app sent. AppCensus does the transmission side commercially. A location or advertising kit
found this way is the capability; the investigation is what showed the capability routinely becoming a sale.

Leaks add snapshots, not a register. The Gravy Analytics breach of January 2025 put around 30 million location points
into circulation, drawn from popular apps including Flightradar, Grindr and Tinder, which is a photograph of one
broker's holdings rather than a list anyone maintains.

Practically: check the apps you carry against Exodus, treat a high tracker count as a reason to replace rather than
configure, and read absence as unknown rather than safe.

## If you want to see before you decide

[TrackerControl](https://github.com/OxfordHCC/tracker-control-android) shows which trackers sit in which app and can
block them, using Android's VPN functionality "to analyse apps' network communications locally on the Android device".
Its lists combine "the Disconnect blocklist, used by Firefox" with an in-house one built "from analysing ~2 000 000
apps". For most people it is the better first install than a general firewall, because the report is the useful part.

For a fuller picture, [PCAPdroid on a spare handset](pcapdroid.md) captures what a device actually sends, which beats
any on-device summary.

## Picking one blocker

Android allows one app at a time to hold the VPN slot, so a local firewall, a local blocker and a VPN app are mutually
exclusive. That constraint decides more of this than any feature comparison.

* Wanting per-app control and domain blocking on one phone: NetGuard, in the build from
  [the project's own releases](https://github.com/M66B/NetGuard). It can "block each and every application, even system
  applications and components", and its hosts-file blocking closes the third-party route.
* Wanting tracker visibility as well as blocking: TrackerControl, as above. It also states that "other VPNs or Private
  DNS are not supported" while it runs.
* Wanting a firewall, DNS encryption and a WireGuard tunnel in one app:
  [RethinkDNS](https://github.com/celzero/rethink-app), which combines a "DNS over HTTPS / DNS over Tor / DNSCrypt
  client, WireGuard proxifier, firewall, and connection tracker", while saying plainly that it is "not an anonymity
  tool".
* Already running a VPN and unwilling to give it up: do not fight over the slot. Filter at the network instead, with
  NextDNS or Pi-hole from the [blocking playbook](blocks.md), or use a cloud-resolver blocker such as Blokada 6, which
  works on "any platform supporting private DNS" at the cost of routing name resolution through a third party.
* Covering a household rather than a handset: network-level filtering again, since it applies to every device on the
  network and to the ones that cannot run a blocker at all.
* Wanting filtering inside HTTPS: [AdGuard](https://adguard.com/en/adguard-android/overview.html) is the one that does
  it, by generating "a unique root certificate" and installing it in the system so each connection can be decrypted
  locally. A root certificate is a large amount of trust to hand an application, it is not on Google Play by AdGuard's
  own account, and the free version "can't filter apps".

## Making NetGuard actually block trackers

Blocking apps works out of the box. Blocking tracker domains does not, and the conditions are easy to miss.

* Use the release from the project rather than the store version. [The ad-blocking
  documentation](https://github.com/M66B/NetGuard/blob/master/ADBLOCKING.md) states that "ad blocking is not available
  when NetGuard was installed from the Google Play store".
* Enable "Filter traffic", "Block domain names", and "Manage system apps" in advanced options.
* Import or download a hosts file. NetGuard fetches the StevenBlack list by default.

## What none of them fix

* The first-party route. Apps that "have a 'data saver'-like feature that proxies requests through their servers" are
  unaffected by host blocking, and so is any app sending coordinates to its own API. A blocker never sees it, and a
  permission is the only thing that closes it.
* The address. NetGuard "is not meant to, and does not, encrypt your internet traffic or hide your IP address", and DNS
  filtering does not either, so IP-derived location survives everything on this page except a VPN.
* Exact-name matching. Wildcards are not supported, so a tracker that rotates subdomains outlives the list, and a single
  app cannot be exempted "because Android resolves domain names on behalf of all apps".
* Anything already collected. Records sold before today stay sold, and TrackerControl's own disclaimer is the honest
  summary of the whole category: "No app can offer 100% protection against tracking."

If you install nothing else: identifier off, precise location denied, worst two apps gone. That is most of the available
protection, and it costs an afternoon.

Last reviewed: 2026-08-13.
