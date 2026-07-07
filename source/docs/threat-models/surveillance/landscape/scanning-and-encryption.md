# Scanning and encryption

The newest front is inside the message itself.

## Chat Control

Since 2022 the EU has debated a regulation to combat child sexual abuse material, the CSA Regulation, widely known as ["Chat Control"](https://www.patrick-breyer.de/en/posts/chat-control/), that would oblige services to detect illegal material. In its strongest forms it would require scanning the content of private messages, including on end-to-end encrypted services, before or as they are sent. The mechanism is client-side scanning: software on the device inspects content against a database before encryption. That breaks the guarantee that only sender and recipient can read a message, whatever the transport encryption does afterwards.

The proposal has moved in fits. A version requiring mandatory detection, later called "Chat Control 1.0", was rejected by the European Parliament in March 2026, a decision that turned on a single vote. The Council had adopted a position in November 2025 that dropped mandatory client-side scanning but kept a permanent voluntary-scanning framework, age-verification duties reaching encrypted services, and risk-mitigation obligations broad enough to pressure encrypted services into changing how they work. A successor package, "Chat Control 2.0", was in trilogue negotiation through 2026; at the time of writing its final shape is not settled.

## The wider pressure on encryption

Chat Control is one expression of a longer campaign, framed by some agencies as the "going dark" problem: the demand that strong encryption carry a lawful-access route for authorities. The technical objection has not changed. A mechanism that lets an authorised party read encrypted content is a mechanism others can find and misuse, and there is no known way to build access for one reader that cannot become access for another. The separate ePrivacy Regulation, meant to modernise the rules on confidentiality of communications, has stalled for years in the same tension.
