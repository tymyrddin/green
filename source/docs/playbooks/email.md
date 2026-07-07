# Protecting email privacy

Email often carries hidden tracking and metadata that reveal more than the message itself: whether it was opened, an approximate location, even device details. A few changes close most of that.

## Choose a privacy-focused provider

Providers differ in how they treat data. The more private options include:

* ProtonMail (Switzerland): strips metadata, encrypts message content, and does not track activity, with free accounts available.
* Tutanota (Germany): end-to-end encryption and no third-party tracking.
* Skiff: encrypted and open-source, with aliases that hide the real address.

Gmail, Outlook and Yahoo scan mail for advertising and profiling, and are worth avoiding for anything sensitive.

## Stop senders tracking opens

Many senders embed an invisible tracking pixel to record when a message was opened, an approximate location, and the device in use. Blocking it takes three habits:

* Turn off automatic loading of external images. Gmail, Outlook and Apple Mail all have the setting, and it stops most pixels loading.
* Add a tracker blocker such as PixelBlock for Gmail or TrackerControl.
* Read in plain-text mode where the client supports it, which loads no tracking elements at all.

## Remove metadata before forwarding

A forwarded email can carry hidden metadata such as sender IP addresses and timestamps. Copying the text into a fresh message or document drops it. For attachments, ExifTool on the command line or Metadata Cleaner as a GUI tool scrubs files before they go out.

## Use aliases for sign-ups

Handing out an alias rather than the real address limits linkage:

* SimpleLogin or AnonAddy create instant aliases that forward to the main inbox.
* ProtonMail's "+" aliases add a suffix (name+shop@protonmail.com) that filters and blocks spam.
* Temp-Mail.org or Guerrilla Mail cover one-time sign-ups.

## Secure the account

A private provider still exposes mail if the account itself is taken:

* Enable two-factor authentication with an authenticator app such as Authy rather than SMS.
* Review recent-login activity, which most providers show.
* Use a strong, unique password, generated and stored in a manager such as Bitwarden or KeePass.

## Watch for phishing

Some mail exists to extract personal data. The recurring tells are urgent demands ("the account will be closed"), sender addresses that do not match the apparent origin, and requests for passwords or payment details. When a message is in doubt, contacting the company directly beats following its links.

## Encrypt sensitive mail

For genuinely confidential messages, ProtonMail and Tutanota encrypt by default, and PGP through a tool such as GPG Suite covers manual encryption for more advanced use.
