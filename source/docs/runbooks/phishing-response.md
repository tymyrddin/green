# Phishing click response

Trigger: a link clicked and realised too late as not what it claimed, credentials entered on a site that turned out to be fake, an attachment opened with unusual behaviour, or a security tool flagging a clicked link as malicious.

Speed is what counts here. The window between the click and an attacker acting on credentials is often minutes, not hours.

## Change the password immediately

If credentials (username, password or 2FA code) went into a suspicious site, change that account's password right now, before anything else. The attacker may already hold the credentials but not yet have had time to use them.

Work from a device and network known to be clean. After a click on a work device, consider changing the password from a personal device while the work device is investigated.

## Revoke sessions

After the password change, revoke all active sessions on the account, usually under Security or Devices in settings. This logs out any session the attacker may have started with the stolen credentials.

A 2FA code entered on the fake site was a one-time token and is now spent. If the attacker used it quickly enough to log in, though, they may hold an active session, which revoking sessions closes.

## Assess what was exposed

Which account was targeted, and what data or access does it hold?

If it was email: treat it as in the [account compromise runbook](account-compromise.md), watching in particular for follow-on attacks against accounts that use it for recovery.

If it was a work account: notify the organisation's security team immediately, without waiting to see whether anything happened.

If payment card details were entered: contact the bank to report the potential fraud and request a new card.

## Investigate the device

A click does not always mean only credentials were taken. Malicious links sometimes deliver malware or browser exploits.

If the click led to a page asking for a download, or the page behaved strangely (unexpected pop-ups, a blank page, the browser crashing), treat the device as potentially compromised and follow the [device compromise playbook](../playbooks/device-compromise.md).

If the only thing entered was credentials on a convincing but inert fake page, the device itself is probably clean; a reputable malware scan confirms it.

## Report the phishing attempt

Report the URL to:
- Google Safe Browsing (safebrowsing.google.com/safebrowsing/report_phish/)
- The email provider, if it arrived by email (most have a "Report phishing" option)
- The organisation being impersonated, if it was a brand phish aimed at their customers

Reporting helps get the domain taken down and protects others who receive the same message.

A targeted attack, where the message carried accurate personal details rather than a generic mass lure, is a different threat level. Report it to an organisation's security team, or for an individual, weigh whether the surveillance threat models on this site describe the situation.

Last reviewed: 2026-07-08.
