# Harden a phone for privacy

A phone arrives set up for convenience, not for privacy. The defaults favour data collection, cross-app tracking, and
cloud copies of almost everything. A handful of changes close the widest gaps without turning the device into a chore to
use.

The menu paths below were current on iOS 26 and Android 16, and Apple and Google move things between versions, so treat the names as a guide and search Settings if a path has shifted.

## Start with the account, not the phone

Most of what a phone knows about you is held in the account behind it, the Apple ID or the Google account, not on the
handset. That is the place to start.

On a Google account, [myaccount.google.com](https://myaccount.google.com) has a Data and Privacy section where Web and
App Activity, Location History, and ad personalisation can each be turned off and set to auto-delete. On an Apple ID,
Settings, your name, then Privacy and the analytics and advertising options do the equivalent. Turning these off does
more than any single on-device toggle, because it changes what is collected in the first place.

## Lock the screen and encrypt the storage

A device that is not locked is not private, and on modern phones the lock is also what encrypts the storage.
The [device encryption runbook](../runbooks/device-encryption.md) covers this: on iOS, encryption is on whenever a
passcode is set (an alphanumeric passphrase is stronger than a six-digit PIN); on Android, a screen lock enables it on
recent devices.

One judgement call sits here. Biometric unlock (face or fingerprint) is convenient, but a PIN or passphrase carries more
legal protection in situations where unlocking might be compelled, such as a border crossing.
The [travel devices playbook](travel-devices.md) goes into when that trade-off is worth making.

## Cut off the advertising identifier and cross-app tracking

Every phone ships with an advertising ID that lets apps and networks link your activity into one profile.
The [advertising ID runbook](../runbooks/adids.md) covers turning it off: on iOS, Settings, Privacy and Security,
Tracking, and switch off "Allow Apps to Request to Track"; on Android, Settings, Privacy, Ads, and delete the
advertising ID outright.

## Review what your apps can reach

Permissions accumulate quietly. An app granted location or microphone access once keeps it until you take it back.

On Android, the Permission Manager (Settings, Security and Privacy, then Privacy controls, or Settings, Apps, Permission
Manager, depending on the make) lists every permission by category and shows which apps hold it. The Privacy Dashboard,
alongside it, shows what was actually used in the last several days. It is worth turning on "Remove permissions if app
is unused" so that anything you stop using loses its access automatically.

On iOS, Settings, Privacy and Security holds the same information one category at a time (Location Services, Microphone,
Camera, and so on). For location in particular, "While Using the App" or "Ask Next Time" is usually enough, and
background location is rarely needed. Stripping location from the camera is covered separately in
the [photos runbook](../runbooks/photos.md).

## Lock down the browser

The browser is where most tracking actually happens. The [blocking tracking scripts playbook](blocks.md) covers content
blockers; the [Chrome hardening playbook](chrome.md) and
the [Chrome Topics runbook](../runbooks/disable-chrome-topics.md) cover the settings that turn off interest profiling.
On a phone, a privacy-respecting browser with tracker blocking built in saves configuring one by hand.

## Encrypt what leaves the phone

The handset may be encrypted, but its backups often are not. This is the step most people miss.

On iOS, Advanced Data Protection extends end-to-end encryption to iCloud backups, photos, and notes, so that not even
Apple can read them. Turn it on under Settings, your name, iCloud, then Advanced Data Protection; it first asks you to
set a recovery contact or recovery key, because with it enabled Apple can no longer reset your access for you. Keep that
recovery key somewhere physically safe.

On Android, a Google account backup is encrypted with your device screen lock, which is reasonable; for a stronger
separation, some people keep sensitive material off cloud backup altogether.

## Logins: passkeys and a second factor

Once the device is in order, the accounts on it are the next layer. The [passkeys runbook](../runbooks/passkeys.md) and
the [authenticators runbook](../runbooks/authenticators.md) cover moving away from reusable passwords and adding a
second factor that is not SMS.

## Messaging

Standard SMS and most chat apps are not private. The [encrypted messaging playbook](messaging.md) covers moving
sensitive conversations to Signal.

## If someone may already have access

Hardening a phone assumes you are the only one with access to it. If that is not certain, for example after a
relationship in which someone else set up or handled the device, the order changes and some steps can tip the other
person off. iOS has a Safety Check (Settings, Privacy and Security, Safety Check) built for exactly this, which reviews
and can reset who and what has access. Start with the [survivor strategy](../strategy/survivors.md) and
the [audit shared accounts playbook](audit-shared-accounts.md) first.

Last reviewed: 2026-07-08 (iOS 26, Android 16).
