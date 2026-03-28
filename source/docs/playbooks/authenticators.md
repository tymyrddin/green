# Enable two-factor authentication

A password on its own is one gate. Two-factor authentication (2FA) adds a second, so that
knowing the password is no longer sufficient to get in. Even if your password is leaked in
a breach, an attacker without your second factor cannot log in.

SMS-based 2FA is better than nothing. It is also the weakest form available, vulnerable to
SIM-swapping (where an attacker convinces your mobile carrier to transfer your number to a
device they control). Use an authenticator app instead wherever possible.

## Choose an authenticator app

Aegis (Android, free, open source): allows encrypted backups of your codes, which matters
a great deal when you eventually replace your phone.

Raivo (iOS, open source): similar to Aegis for Apple devices.

Ente Auth (Android and iOS, open source, optional encrypted cloud sync): good if you want
your codes to survive a lost phone without a local backup.

Avoid authenticator apps tied to a single vendor account (such as Google Authenticator in its
earlier versions) unless you are certain you can back up and restore the codes.

## Start with email

Enable 2FA on your email account before anywhere else. Your email is the recovery path for
almost everything else. If someone gets into your email, they can reset the passwords on every
other account.

Most email providers have 2FA under account security settings. Look for "two-step verification"
or "authenticator app."

When you add a new account to your authenticator app, you will be shown a QR code. Scan it.
You will also be shown backup codes: save these somewhere secure, separately from your
authenticator device. They are what you use if you lose your phone.

## Roll out to other accounts

In roughly this order:

1. Password manager (if you use Bitwarden or similar, this is critical)
2. Banking and financial services
3. Work accounts
4. Social media (especially if you use these for login elsewhere)
5. Everything else

Most services have 2FA under a "Security" or "Privacy" section in account settings. If a
service does not offer 2FA, consider whether you should trust it with sensitive information.

## Hardware keys

For higher-threat situations, a hardware security key (such as a YubiKey) is more resistant
to phishing than an authenticator app, because the key will only respond to the genuine site
it was registered with. It will not hand over a code to a convincing fake.

Hardware keys work well as a second 2FA method on top of an authenticator app: use the app
for daily convenience, register the key as a backup.
