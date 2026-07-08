# Enable two-factor authentication

A password on its own is one gate. Two-factor authentication (2FA) adds a second, so that knowing the password is no longer enough to get in.

SMS-based 2FA is better than nothing, but it is the weakest form available, vulnerable to SIM-swapping, where an attacker persuades a mobile carrier to move the number to a device they control. An authenticator app is preferable wherever possible.

## Choose an authenticator app

Aegis (Android, free, open source): supports encrypted backups of the codes, which counts for a great deal when a phone is eventually replaced.

Raivo (iOS, open source): similar to Aegis for Apple devices.

Ente Auth (Android and iOS, open source, optional encrypted cloud sync): useful for keeping codes alive across a lost phone without a local backup.

Authenticator apps tied to a single vendor account, such as early versions of Google Authenticator, are worth avoiding unless the codes can definitely be backed up and restored.

## Start with email

Enable 2FA on the email account before anywhere else. Email is the recovery path for almost everything else: someone who gets into it can reset the passwords on every other account.

Most email providers keep 2FA under account security settings, listed as "two-step verification" or "authenticator app".

Adding a new account to an authenticator app shows a QR code to scan, and a set of backup codes. Save the backup codes somewhere secure, separate from the authenticator device; they are the way back in if the phone is lost.

## Roll out to other accounts

In roughly this order:

1. Password manager (critical, for Bitwarden or similar)
2. Banking and financial services
3. Work accounts
4. Social media, especially where it is used to log in elsewhere
5. Everything else

Most services keep 2FA under a Security or Privacy section. A service that offers no 2FA at all is worth a second thought before being trusted with anything sensitive.

## Hardware keys

For higher-threat situations, a hardware security key such as a YubiKey resists phishing better than an authenticator app, because it only responds to the genuine site it was registered with and will not hand a code to a convincing fake.

Hardware keys work well as a second method on top of an app: the app for daily convenience, the key registered as a backup.

That same resistance, answering only to the genuine site, is what passkeys bring to everyday sign-ins; the [passkeys runbook](passkeys.md) covers setting them up.
