# Use encrypted messaging

Standard SMS is not private. The message content passes through your mobile carrier in
plaintext, is retained by them, and is accessible to law enforcement in most jurisdictions
without a warrant. Most consumer messaging apps are no better, and some are considerably
worse.

End-to-end encryption (E2EE) means the message is encrypted on your device and can only be
decrypted by the recipient's device. No one in the middle, not the app company, not your
carrier, not a bulk collection programme, can read the content.

## Signal

Signal is the most widely recommended E2EE messaging application. It is free, open source,
audited, and available on Android, iOS, and desktop.

Install:

1. Download from the App Store or Google Play (or signal.org).
2. Register with a phone number. Signal needs a number to function, but the number is only
   used for registration. You can use a second number or a VoIP number if you prefer not to
   register your primary.
3. Set a registration lock PIN (in Settings > Account) to prevent someone who takes control
   of your number from registering Signal in your name.

Key settings after install:

- Enable disappearing messages by default (Settings > Privacy > Default Timer). A sensible
  default for most people is one week. Sensitive conversations warrant shorter.
- Turn off read receipts and typing indicators if you prefer not to reveal when you are
  active (Settings > Privacy).
- Review linked devices regularly (Settings > Linked Devices) and remove any you do not
  recognise.

Signal can only communicate with other Signal users. It will not fall back to SMS. If a
contact is not on Signal, you will see this clearly before sending.

## What Signal protects and what it does not

Signal protects message content and voice/video call content. It does not hide the fact
that you are communicating with a particular person, nor when, nor at what frequency.
Metadata, who talks to whom and when, is less protected than content. For most everyday
use this is an acceptable trade-off. For situations where even contact metadata is
sensitive, additional precautions are needed.

## WhatsApp

WhatsApp uses the Signal Protocol for content encryption, so the content of messages is
encrypted in transit. However, WhatsApp is owned by Meta and retains metadata: who you
message, when, how often, on what device, from what IP address. This metadata is used
commercially and is shared with law enforcement on request.

For general private conversations with people who are not on Signal, WhatsApp is a
reasonable choice. For conversations where the metadata itself is sensitive, it is not.

## Email

Email is a low-privacy medium by design. It was not built for privacy. Even with transport
encryption (which most email now uses), message content is stored unencrypted on servers
and is accessible to the provider.

For a new, private email account, ProtonMail and Tuta (formerly Tutanota) offer E2EE for
messages between users of the same service, and encrypted storage.

For existing email accounts, PGP encryption is possible but requires the other party to
use it too. It is practical in contexts where both parties are motivated to set it up.
For most people, switching the sensitive conversations to Signal is less friction and
more reliable.
