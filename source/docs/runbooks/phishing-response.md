# Phishing click response

Trigger: you clicked a link and realised too late it was not what it claimed, you entered
credentials on a site that turned out to be fake, you opened an attachment and the behaviour
was unusual, or a security tool has flagged a link you clicked as malicious.

Speed matters here. The window between clicking and an attacker acting on credentials is
often minutes, not hours.

## Change the password immediately

If you entered credentials (username, password, or 2FA code) on a suspicious site, change
the password for that account right now. Do this before anything else. The attacker may
already have the credentials but has not yet had time to use them.

Use a device and network you are confident are clean. If you clicked a link on a work
device, consider whether to use a personal device to change the password while you
investigate the work device.

## Revoke sessions

After changing the password, revoke all active sessions on the account. This is usually
under "Security" or "Devices" in account settings. This logs out any session the attacker
may have started with the stolen credentials.

If the site requested a 2FA code and you entered one, that code was a one-time token and
is now spent. However, if the attacker used it quickly enough to log in, they may have
an active session. Revoking sessions addresses this.

## Assess what was exposed

What account was targeted? What data or access does it hold?

If it was your email: treat it as described in the
[account compromise runbook](account-compromise.md), paying particular attention to
follow-on attacks against accounts that use it for recovery.

If it was a work account: notify your organisation's security team immediately. Do not
wait to see if anything happened first.

If you entered payment card details: contact your bank to report the potential fraud and
request a new card.

## Investigate the device

Clicking a link does not always mean only credentials were stolen. Malicious links sometimes
deliver malware or browser exploits.

If you clicked a link and were taken to a page that asked you to download something, or if
the page behaved strangely (unexpected popups, page appearing blank, browser crashing),
treat the device as potentially compromised and follow the
[device compromise playbook](../playbooks/device-compromise.md).

If you only entered credentials on a convincing but inert fake page, the device itself
is likely clean. Confirm by running a reputable malware scan.

## Report the phishing attempt

Report the URL to:
- Google Safe Browsing (safebrowsing.google.com/safebrowsing/report_phish/)
- Your email provider if it arrived by email (most providers have a "Report phishing" option)
- The organisation being impersonated, if it was a brand phish targeting their customers

Reporting helps get the domain taken down and protects others who receive the same message.

If this was a targeted attack (the message contained accurate personal details about you
rather than a mass-sent generic lure), that is a different threat level. Report it to
your organisation's security team, or if you are an individual, consider whether the
surveillance threat models in this site describe your situation.
