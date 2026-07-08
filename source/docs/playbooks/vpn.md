# VPNs for privacy

A virtual private network (VPN) encrypts internet traffic, hides an IP address, and helps get around censorship. It is one useful layer, though not all VPNs are equal and none is a complete solution.

## What a VPN does

* Hides the IP address, so websites, ISPs and governments see the VPN's location rather than the real one
* Encrypts traffic, which protects data on public Wi-Fi in airports, cafes and hotels
* Bypasses censorship and geo-blocks for news, streaming and social media
* Stops ISP snooping, so the provider cannot log and sell browsing history

## Privacy-focused providers

Proton VPN: Swiss-based, under strong privacy law, with an independently audited no-logs policy, open-source apps, and a free tier that is not speed-throttled (protonvpn.com).

Mullvad: no account needed, payable in cash or cryptocurrency, flat-rate at around €5 a month, running on RAM-only servers that wipe on reboot (mullvad.net).

IVPN: anti-tracking features, WireGuard and multi-hop routing, and no personal data required, aimed at more advanced users (ivpn.net).

NordVPN: a large server network suited to streaming, with built-in threat protection; Panama-based, with repeated independent no-logs audits, though its ownership and jurisdiction draw more scrutiny than the options above (nordvpn.com).

## The risk in free VPNs

Most free VPNs log and sell data (Hola, Turbo), run slowly with ads, or use weak encryption that can leak an IP. The main trustworthy free option is Proton VPN Free, which keeps no logs and imposes no speed limit.

## Setting one up

1. Choose a provider (Proton, Mullvad or IVPN are good defaults)
2. Download and install from the official website rather than an app store
3. Enable the kill switch, which cuts the connection if the VPN drops
4. Use WireGuard or OpenVPN, faster and more secure than older protocols

A leak test at [ipleak.net](https://ipleak.net/) confirms the tunnel is holding.

## Where a VPN does not help

* Against malware, which needs antivirus and a firewall
* Against Google or Facebook tracking, which needs privacy browsers and cookie blockers
* Once logged into an account, since a VPN hides an IP, not an identity

## Further notes

* Chaining a VPN through Tor raises anonymity at the cost of speed
* US-based VPNs sit under surveillance law worth weighing
* An independent no-logs audit is the claim worth checking

Proton VPN or Mullvad suit a privacy-first setup; NordVPN favours speed and streaming. A VPN is one layer, best combined with [Firefox and uBlock Origin](blocks.md) and [encrypted email](email.md).
