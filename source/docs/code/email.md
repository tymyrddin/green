# Email header analysis

Every email carries more than its message. The headers record the journey: which servers handled it, in what order, from what IP addresses, and at what exact times. Reading them traces the route from sender to recipient and often reveals the sender's real location even when they tried to hide it.

The "From" field shows whoever the sender chose to display. The headers show what the servers actually recorded. Any recipient can read them. No special access is required.

## How it works

Each server that handles an email adds a "Received" header to the top of the message as it passes through. Reading the Received headers from bottom to top reconstructs the journey in chronological order.

```
for each "Received" header (reading bottom to top):
    extract: originating server name, IP address, timestamp
    check: does the IP resolve to a claimed location?
    check: does the sequence of servers make sense geographically?
    check: does the sender's domain match the IP that first injected the message?
```

An analysis script opens the email file, iterates through every header, and prints the chain. The most revealing part is typically the first Received entry: the server that accepted the message from the sender's device. If the sender used their home internet connection, that IP resolves to their ISP and narrows their location to a city or neighbourhood. If they used a mail client rather than a web browser, the originating IP is often their device's own address.

The "Subject" and "Date" headers, decoded from MIME encoding, confirm the content and timing. Routing anomalies, a message claiming to originate in London but first appearing on a server in an unexpected country, flag mismatches worth investigating.

## What this reveals

Email headers are a log the sender has no control over once the message leaves their hands. An investigator, an adversary, or anyone with basic technical literacy can identify the originating infrastructure, check whether the claimed sender domain is consistent with the originating IP, and trace the path through any intermediate relays.

This is routine in forensic email analysis, in spam filtering, and in phishing investigations. It is also a straightforward tool for identifying the real origin of a message sent under a false name.

## Defences

The most effective defence is using a webmail provider that deliberately strips the originating IP from the first Received header before adding its own. Most large providers do this: a message sent through Gmail or ProtonMail shows the provider's server, not the sender's device. Sending through a remailer or an anonymising mail service adds further layers. The key is ensuring that no Received header in the chain points directly to infrastructure the sender controls or occupies.
