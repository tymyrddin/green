# Set up a password manager

Reusing passwords is the single most reliably exploited vulnerability in everyday digital life.
When one service is breached, every other service with the same password is compromised too.
A password manager solves this by generating and storing a unique password for every account,
so you only need to remember one strong passphrase.

## Choose a manager

Three solid options, in order of preference by threat model:

Bitwarden: open source, free tier covers all basic needs, can be self-hosted if you prefer not
to trust their servers. Audited. Available on all platforms.

KeePassXC: open source, stores the vault as a local file only. Nothing leaves your device
unless you choose to sync it yourself. Good if you do not want cloud storage at all.

1Password: polished commercial option with strong security record. Not free, but inexpensive.
Suitable for people who want something that works without configuration.

## Set up Bitwarden

1. Go to bitwarden.com and create an account using an email address you control.
2. Choose a master passphrase: at least four random words strung together, not a phrase you have
   used before. Write it down and store it somewhere physically secure until you have it memorised.
   This is the one thing you cannot recover if you lose it.
3. Install the browser extension for your primary browser.
4. Install the mobile app on your phone.
5. Enable two-factor authentication on the Bitwarden account itself before you start adding
   passwords. See the [authenticators playbook](authenticators.md) for how.

## Migrate existing passwords

If your browser has saved passwords, export them:

- Chrome: Settings > Passwords > Export
- Firefox: about:logins > Export logins

Import the file into Bitwarden (Settings > Import data). Then delete the exported file
and clear saved passwords from the browser.

After import, go through your accounts in order of importance and change any passwords that
were reused or are shorter than 16 characters. Bitwarden's generator will create something
suitably incomprehensible.

## After setup

When creating any new account, use the browser extension to generate a password immediately.
Never type one yourself. If you are in a hurry and type one yourself, you will either reuse
something or pick something weak. The generator takes three seconds.

Check periodically whether any of your accounts have appeared in a known breach. Bitwarden
integrates with Have I Been Pwned and will flag compromised passwords in the vault.
