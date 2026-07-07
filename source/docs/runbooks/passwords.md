# Set up a password manager

Reusing passwords is the single most reliably exploited weakness in everyday digital life. When one service is breached, every other service with the same password falls with it. A password manager solves this by generating and storing a unique password for every account, leaving only one strong passphrase to remember.

## Choose a manager

Three solid options, in order of preference by threat model:

Bitwarden: open source, a free tier that covers all the basics, and self-hostable for anyone who prefers not to trust its servers. Audited. Available on every platform.

KeePassXC: open source, storing the vault as a local file only. Nothing leaves the device unless it is synced deliberately. Good where cloud storage is unwanted entirely.

1Password: a polished commercial option with a strong security record. Not free, but inexpensive, and suited to anyone who wants something that works without configuration.

## Set up Bitwarden

1. Go to bitwarden.com and create an account with an email address that is not shared with anyone else.
2. Choose a master passphrase: at least four random words strung together, not one used before. Write it down and store it somewhere physically secure until it is memorised. This is the one thing that cannot be recovered if lost.
3. Install the browser extension for the primary browser.
4. Install the mobile app.
5. Enable two-factor authentication on the Bitwarden account itself before adding any passwords (see the [authenticators runbook](authenticators.md)).

## Migrate existing passwords

Browser-saved passwords can be exported:

- Chrome: Settings, Passwords, Export
- Firefox: about:logins, Export logins

Import the file into Bitwarden (Settings, Import data), then delete the exported file and clear the saved passwords from the browser.

After import, work through the accounts in order of importance and change any password that was reused or is shorter than 16 characters. Bitwarden's generator produces something suitably incomprehensible.

## After setup

When creating any new account, generate the password from the browser extension straight away, rather than typing one by hand. A hand-typed password under time pressure tends to be reused or weak; the generator takes three seconds.

Check periodically whether any account has appeared in a known breach. Bitwarden integrates with Have I Been Pwned and flags compromised passwords in the vault.
