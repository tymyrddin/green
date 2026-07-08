# Set up passkeys

A passkey replaces the password-and-code pair with a single credential that cannot be phished. Under the surface it is a cryptographic key pair: the service holds the public half, and the private half stays on your device or in your password manager and signs a challenge when you sign in. There is nothing to type, nothing to reuse, and nothing to hand over to a convincing fake, because a passkey only answers to the site it was created for.

The fingerprint, face scan, or PIN that confirms a passkey never leaves the device. It unlocks the key locally; the service sees only the signature.

## Decide where passkeys will live

This is the real decision, because it determines what happens when a device is lost.

A password manager (Bitwarden and 1Password both support passkeys) keeps them next to the passwords, syncs them across platforms, and avoids tying sign-in to a single vendor. For anyone already running the [password manager runbook](passwords.md), this is the natural home, and recovery is the vault recovery you already have: master passphrase plus the manager's own 2FA.

Platform storage (iCloud Keychain, Google Password Manager, Windows Hello) is built in and convenient, but binds accounts to that ecosystem, and recovery runs through that vendor's account recovery. Moving passkeys out again is only starting to become possible, so this is a longer commitment than it looks.

A hardware key such as a YubiKey stores passkeys on the key itself, with nothing synced anywhere. Strongest isolation, and suited to high-threat situations, but a lost key means lost passkeys: register two and keep one somewhere physically safe.

## Start with email

Email is the recovery path for almost everything else, which makes it the right first account here for the same reason it was in the [authenticators runbook](authenticators.md).

1. Open the account's security settings. The option is usually called "passkeys" or "create a passkey".
2. When the browser or phone asks where to store it, check the prompt before confirming: browsers frequently default to platform storage. If the plan is the password manager, make sure its extension is handling the prompt.
3. Confirm with the device unlock.
4. Sign out, or open a private window, and sign back in with the passkey to confirm it works.
5. If the service offers backup codes, save them somewhere secure and separate from the passkey.

## Roll out to other accounts

The same order as 2FA: banking and financial services, work accounts, social media, then everything else. Adoption is uneven. Some services support passkeys fully, some accept them only as a second factor next to a password, and a long tail offers nothing yet. Passkeys arrive account by account, not as a single migration, so the password manager and authenticator app stay in service for the rest.

Where a service allows more than one passkey, register a second from a different device or key. It is the cheapest recovery plan available.

## The password stays, for now

Most services keep password sign-in as a fallback after a passkey is added, which means the account remains only as strong as its weakest way in. The passkey still earns its place: day-to-day sign-ins stop being phishable, and there is no code to be talked out of. When a service offers to disable password sign-in or weaker recovery methods, that is worth taking, once the passkey demonstrably works on every device you sign in from and a second passkey or backup codes exist.
