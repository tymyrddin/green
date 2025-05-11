# Quantum-resistant encryption: Why your secrets need future-proofing today

The bad news: Quantum computers are coming, and 
[they’ll shred today’s encryption like wet tissue paper](../state/quantum.md). The good news: 
Privacy apps like Signal and ProtonMail are already deploying post-quantum cryptography (PQC) to keep your data safe. 
Here’s why it matters—and how to use it.

## The Quantum apocalypse (for your privacy)

Today’s encryption (like RSA and ECC) relies on math problems that quantum computers could solve in seconds. Once 
they are powerful enough:

* Every intercepted Signal message could be retroactively decrypted.
* Old PGP-encrypted emails might as well be postcards.
* [Government agencies are already harvesting data to crack later](../state/surveillance) ("Store Now, Decrypt Later" attacks).

When Will It Happen?

* 5–15 years for large-scale quantum computers (per NIST).
* But military/govt data is being collected NOW for future decryption.

## How Quantum-resistant encryption works

PQC uses new math problems that even quantum computers struggle with, like:

* Lattice-based cryptography (Signal’s PQXDH)
* Hash-based signatures (ProtonMail’s quantum-resistant PGP)

Think of it as upgrading from a wooden door to a vault lined with alien alloy.

## Apps already using PQC (and how to enable it)

Signal (PQXDH Protocol)

* Automatically enabled since 2023 (no user action needed).
* Mixes traditional encryption with CRYSTALS-Kyber (a lattice-based algorithm).
* Why it’s cool: Even if someone records your chats today, they can’t crack them later.

ProtonMail (Post-Quantum PGP)

* Manual setup: Compose an email → Click the "Quantum-safe" padlock (if recipient also uses PQC).
* Uses CRYSTALS-Dilithium for signatures.
* Limitation: Only works if both parties enable it.

Other early adopters

* iMessage (Apple’s PQ3 protocol, rolling out in 2024).
* Tuta (formerly Tutanota, working on hybrid encryption).

## What you can do today

* Switch to Signal/ProtonMail if you haven’t already.
* For PGP users: Generate a quantum-resistant key with (Requires GnuPG 2.4+):

```bash
    gpg --quick-gen-key "Your Name" future-default
```

* Don’t panic—but assume any non-PQC data could be readable by 2040.

## The fine print

* Not all PQC is battle-tested yet. Some algorithms might have flaws (NIST is still finalizing standards).
* Old devices may not support it. Check your app versions.
* VPNs/SSL will need upgrades too. Most web traffic is still vulnerable.

Encrypt like the future depends on it (because it does).

Quantum computing won’t just break crypto—it’ll rewrite privacy, finance, and cybersecurity. By using PQXDH and 
quantum PGP now, you’re locking the vault before the thieves get the tools.
