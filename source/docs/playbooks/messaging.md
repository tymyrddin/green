# Use encrypted messaging

Standard SMS is not private. The message content passes through the mobile carrier in plaintext, is retained by them, and is accessible to law enforcement in most jurisdictions without a warrant. Most consumer messaging apps are no better, and some are considerably worse.

End-to-end encryption (E2EE) means the message is encrypted on the sender's device and can only be decrypted by the recipient's device. No one in the middle, not the app company, not the carrier, not a bulk collection programme, can read the content.

## Signal

Signal is the most widely recommended E2EE messaging application. It is free, open source, audited, and available on Android, iOS and desktop.

Install:

1. Download from the App Store or Google Play (or signal.org).
2. Register with a phone number. Signal needs a number to function, but the number is only used for registration. A second number or a VoIP number works for anyone who prefers not to register a primary line.
3. Set a registration lock PIN (Settings, then Account) so that someone who takes control of the number cannot register Signal in the owner's name.

Key settings after install:

- Enable disappearing messages by default (Settings, Privacy, Default Timer). One week is a sensible default for most people; sensitive conversations warrant shorter.
- Turn off read receipts and typing indicators to avoid revealing when the account is active (Settings, Privacy).
- Review linked devices regularly (Settings, Linked Devices) and remove any that are unfamiliar.

Signal only communicates with other Signal users. It does not fall back to SMS, and a contact who is not on Signal is shown clearly before sending.

## What Signal protects and what it does not

Signal protects message content and voice and video call content. It does not hide the fact that a particular person is being contacted, nor when, nor how often. Metadata, who talks to whom and when, is less protected than content. For most everyday use this is an acceptable trade-off. Where even contact metadata is sensitive, additional precautions are needed.

## WhatsApp

WhatsApp uses the Signal Protocol for content encryption, so message content is encrypted in transit. WhatsApp is owned by Meta, however, and retains metadata: who is messaged, when, how often, on what device, from what IP address. That metadata is used commercially and is shared with law enforcement on request.

For general private conversations with people who are not on Signal, WhatsApp is a reasonable choice. Where the metadata itself is sensitive, it is not.

## Email

Email is a low-privacy medium by design. It was not built for privacy. Even with transport encryption, which most email now uses, message content is stored unencrypted on servers and is accessible to the provider.

For a new, private email account, ProtonMail and Tuta (formerly Tutanota) offer E2EE for messages between users of the same service, and encrypted storage.

For existing email accounts, PGP encryption is possible but requires the other party to use it too. It is practical where both parties are motivated to set it up. For most people, moving the sensitive conversations to Signal is less friction and more reliable.

Last reviewed: 2026-07-08.
