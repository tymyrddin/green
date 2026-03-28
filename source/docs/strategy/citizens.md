# Citizens

Most people's mental model of who is watching them and why is at least a decade out of date. It was formed
during an era of dial-up connections and desktop computers, updated occasionally by news events, and has not
kept pace with the infrastructure that now processes their data as a matter of routine. The threat is not
that someone has decided to target you. The threat is that you have already been included in systems
designed to collect everyone.

This matters for how you respond. Defending against targeted surveillance requires different tools than
minimising your footprint in bulk collection. Most citizens face the second problem more than the first.

## What you are actually defending against

Commercial data brokers have assembled profiles on the majority of adults in most developed countries.
These profiles include location history, purchasing patterns, inferred beliefs and relationships, and
in many cases health indicators. This data is bought and sold without most people's knowledge and is accessible
to law enforcement in many jurisdictions without a warrant, because purchasing data from a broker is not
the same as requesting it under legal process.

The [surveillance infrastructure](../threat-models/surveillance/index.rst) described in the threat models is not
abstract. You are already in it. The question is what surface area you present and whether the data about you is
accurate, correctable, and bounded.

Most threats to individual citizens come not from active targeting but from exposure: data collected for
one purpose used for another, breaches that expose credentials, inferences drawn from aggregated signals
that no single piece of data would support. Defending against these is less about hiding and more about
reducing unnecessary accumulation.

## What to actually do

### Accounts and identity

Your email account is the root of your digital identity. Every password reset, every recovery flow, every
account backup routes through it. A compromised email account is a compromised everything. Treat it
accordingly.

Use a strong, unique passphrase. Enable two-factor authentication using an authentication app, not SMS.
SMS-based authentication is better than nothing but is vulnerable to SIM-swapping. If your threat level
is higher, use a hardware security key.

Use a password manager. Reusing passwords across services is the single most common vector for account
compromise, and it is the most straightforwardly preventable. Pick one manager and use it everywhere.

Separate your high-value accounts from your casual ones. The email address you give to retailers and
newsletters does not need to be the email address that controls your banking.

### Devices

Enable full-disk encryption on your laptop. This is the default on modern MacOS and increasingly on
Linux; on Windows it requires BitLocker or an equivalent. An unencrypted laptop can become a lost laptop
that becomes a full data breach.

Keep software updated. A significant proportion of exploits target vulnerabilities with patches
available. Updated software does not make you invulnerable; it removes you from the large pool of easy
targets.

For mobile, enable screen lock and disable biometric unlock if you face environments where you may be
compelled to unlock your device. A PIN cannot be compelled under UK law in the same way as a
fingerprint, though this varies by jurisdiction.

### Communications

For private communications, use a messaging application with end-to-end encryption enabled by default.
Signal does this. WhatsApp does this for content but not for metadata, which is retained and accessible.
Standard SMS does not.

For email, accept that email is inherently a low-privacy medium and behave accordingly. End-to-end
encrypted email exists and is improving, but requires both parties to use it.

### Data footprint

Delete old accounts. A service you used once in 2014 has data about you and is a breach liability.
Most services provide account deletion under GDPR if you are in the EU.

Audit what apps have access to your location, contacts, and microphone. Mobile operating systems now
provide this visibility. The question to ask for each permission is whether the app's core function
requires it, and if not, revoke it.

Use a browser extension that blocks third-party trackers. Most browsing behaviour is observed by
parties with no relationship to the site you are visiting. The data collected is used to build profiles
that are sold or available for purchase by a range of actors beyond advertisers.

## What gets in the way

Security fatigue is real and it is rational. Most security recommendations are presented as if the
reader has infinite time, moderate technical skill, and no resistance to friction. People who encounter
this framing and find it unrealistic do not usually conclude that the security is wrong. They conclude
that the security is not for them and stop engaging.

The correct response to this is not to lower standards but to sequence changes. An overwhelming list of
things to fix produces inaction. A short list of high-leverage changes produces movement.

If you do one thing: use a password manager and enable two-factor authentication on your email account.
These two changes reduce your exposure to the most common compromise vectors more than any other single
action. Everything else can follow, in whatever order makes sense given your life.

Fear also gets in the way, in the opposite direction. The feeling that surveillance is total and
inescapable produces the same paralysis as exhaustion. The surveillance infrastructure is extensive,
but it is not monolithic. Reducing your surface area is useful even when you cannot eliminate
exposure entirely. A greenhouse with better locks is safer than one with no locks, even if the walls
remain glass.

## The structures working against you

The data broker market operates largely without consumer consent or awareness because the political
and regulatory conditions permit it. The data you provide to one service is sold to others under terms
that are technically disclosed and practically unreadable. This is a structural condition, not a
personal failing.

Understanding this matters because it calibrates where personal action is effective and where
collective or political action is required. Opting out of individual data broker profiles is possible
but laborious and incomplete. The underlying market continues regardless. Personal hygiene helps;
structural reform is the durable fix.

Supporting organisations that advocate for data protection rights is not separate from personal
security. It is part of it. The regulatory frameworks that constrain commercial data collection were
built through political effort, not individual opt-outs, and they require continued effort to maintain
and extend.

## Playbooks

* [Set up a password manager](../runbooks/passwords.md)
* [Enable two-factor authentication](../runbooks/authenticators.md)
* [Use encrypted messaging](../playbooks/messaging.md)
* [Enable device encryption](../runbooks/device-encryption.md)
* [Keep anonymous data separate from your identity](../playbooks/identity.md)
* [Remove yourself from data broker sites](../playbooks/brokers.md)
* [Minimise long-term data storage](../playbooks/minimise.md)
* [Protect your email privacy](../playbooks/email.md)
* [Use a VPN](../playbooks/vpn.md)
* [Block tracking scripts](../playbooks/blocks.md)
* [Disable Chrome's Topics API](../runbooks/disable-chrome-topics.md)
* [Reset your advertising ID](../runbooks/adids.md)
* [Isolate IoT devices with a guest network](../runbooks/vlan.md)
* [Use privacy-focused payment methods](../playbooks/payment.md)
* [Strip metadata from photos](../runbooks/photos.md)
* [Remove metadata from files](../playbooks/files.md)
* [Foil facial recognition](../playbooks/bigbrother.md)
* [Understand quantum-resistant encryption](../playbooks/quantum.md)
* [Submit a GDPR deletion request](../runbooks/gdpr-deletion.md)
* [Prepare devices for high-risk travel](../playbooks/travel-devices.md)

## Runbooks

* [Account compromise response](../runbooks/account-compromise.md)
* [Suspected device compromise](../playbooks/device-compromise.md)
* [Phishing click response](../runbooks/phishing-response.md)
* [Doxxing response](../runbooks/doxxing-response.md)
