# The age-verification app that verified little

The EU's answer to online age checks, an app built on the European Digital Identity wallet and promoted as privacy-preserving, became its own case study when security researchers took it apart. The tool meant to prove a user's age without exposing their identity turned out to weaken both.

## What researchers found

Within about two minutes of the app being presented, the security researcher Paul Moore [showed that its PIN could be defeated](https://www.heise.de/en/news/EU-age-verification-app-Worry-free-package-with-security-vulnerabilities-11262921.html): the codes were insufficiently protected, the rate limits could be reset by editing simple configuration files, and biometric authentication could be switched off with a single change. The researcher Baptiste Robert reproduced the bypass, and the cryptographer Olivier Blazy pointed out a design flaw that no patch closes, that an already-unlocked app on one person's phone will verify someone else's age just as readily.

Separate analysis reported that the identity data did not stay protected either: [facial images read from a passport chip](https://cybernews.com/security/eu-age-verification-app-hack/) over NFC were written to disk unencrypted, and selfie images used for the check were kept rather than deleted. For a system whose entire promise was that sensitive biometric data would not linger, that is the sharpest failure, and the one the "highest privacy standards" framing least survives.

## Why it counts

This case turns not on an adversary reaching data they were not meant to have but on the state building the exposure itself. When the Commission responded that testers had used an outdated demo, the researchers disputed it, and the deeper problem remained: an official tool, held up as the privacy-respecting option, shipped with the flaws it was meant to rule out. Official [digital infrastructure](../vectors.md) is not automatically safer than the commercial kind. It is a surface like any other.
