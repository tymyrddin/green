# Suspected device compromise

Trigger: you found an application you did not install, your device is behaving strangely
(unexpected battery drain, unusual data usage, running hot without obvious cause), you
have reason to believe someone installed monitoring software (a partner, employer, or
unknown party), or a security scan flagged something.

In a domestic abuse context, this scenario requires particular care. Acting on a compromised
device before you have a safe alternative communications channel can alert the abuser that
you know. Read through this runbook fully before taking action.

## Before you act: safety first

If you suspect a partner or other person with physical access has installed monitoring
software, the most dangerous thing you can do is act on the compromised device in a way
that signals you have discovered it.

Do not search for information about stalkerware on the suspected device. Do not message
anyone about it from the suspected device. Establish a safe channel first: borrow a
trusted person's phone or use a device the suspected party has no access to.

Contact a domestic abuse support organisation before acting on the device if this applies
to your situation. Decisions about when and how to remove monitoring software involve
safety considerations that go beyond the technical.

## What to check

On Android, signs of stalkerware include:
- Apps you do not recognise in Settings > Apps.
- An elevated battery usage entry for an unfamiliar process.
- High data usage by an unfamiliar app (Settings > Network > Data usage).
- The device administration apps list showing something you did not add
  (Settings > Security > Device admin apps).

On iOS, the attack surface is narrower without a jailbreak. Signs of concern include:
- Profiles you did not install (Settings > General > VPN & Device Management).
- Unusual battery and data usage patterns.
- If the device was ever out of your physical control, assume a profile may have been installed.

## Decide: investigate or clean slate

Forensic investigation of the device can reveal what was installed and when, which may
matter for legal purposes. If you are working with law enforcement or a legal adviser, do
not wipe the device before they have had a chance to advise.

For most situations: the cleanest path is a factory reset and starting from scratch.
Stalkerware and persistent malware are designed to survive casual removal attempts.
A reset removes them reliably.

Before resetting, back up only what you need and are confident is clean: contacts, photos
(check these for embedded malware if they were received from the suspected attacker), and
documents you created yourself. Do not restore from a full backup, as it may reintroduce
the compromise.

## After cleaning the device

Change passwords for every account that was accessible on the device. Revoke tokens.
Check account settings for backdoors added during the compromise period (recovery addresses,
connected apps, forwarding rules) as described in the
[account compromise runbook](account-compromise.md).

Set up new security practices from the start: full-disk encryption, a clean password manager
installation, 2FA on all accounts.

If the device was a work device, notify your organisation's security team. They may need
to assess whether any organisational data was exposed.
