# Quantum-resistant encryption

Large quantum computers do not exist yet, but the timeline is short enough to plan around. When they arrive, they will break the public-key cryptography (RSA, ECC) that protects most traffic today. Several privacy tools have already moved to post-quantum cryptography (PQC), so the useful actions mostly come down to using them.

## Store now, decrypt later

Today's public-key schemes rest on maths problems a capable quantum computer could solve quickly. Once that threshold is reached:

* Intercepted messages recorded today could be decrypted retroactively.
* Old PGP-encrypted email would offer little protection against a later break.
* Some agencies already collect encrypted traffic to decrypt later, the pattern known as "store now, decrypt later".

NIST's estimates put large-scale quantum computers roughly five to fifteen years out. The collection of encrypted data for future decryption is happening now, which is why forward secrecy against that future is worth having today.

## The mechanism

PQC replaces the vulnerable maths with problems that stay hard for quantum computers, mainly:

* Lattice-based key exchange, the basis of Signal's PQXDH
* Hash-based and lattice-based signatures, used in quantum-resistant PGP

The shift is less a new lock than a new class of lock, chosen because the old class is expected to open.

## Tools that already use it

Signal (PQXDH): enabled by default since 2023, no action needed. It combines a traditional exchange with CRYSTALS-Kyber, so a chat recorded today resists a later quantum break.

ProtonMail (post-quantum PGP): available when both parties support it, using CRYSTALS-Dilithium for signatures. It applies only when the recipient also has it enabled.

Others: Apple's iMessage PQ3 and Tuta's hybrid encryption are further recent adopters.

## Practical steps

* Moving to Signal or ProtonMail covers most everyday messaging.
* For existing PGP use, GnuPG 2.6 (or the 2.5 development series) can generate a post-quantum key. The 2.4 branch cannot, and has reached end of life; on it, `future-default` still produces a classical key:

```bash
gpg --quick-gen-key "Name" pqc
```

* Treat any non-PQC data as potentially readable in the 2040s.

## Caveats

* Not every PQC algorithm is fully battle-tested; NIST is still finalising standards, and some candidates may yet show flaws.
* Older devices and app versions may not support it, so versions are worth checking.
* Transport security (VPNs, TLS) needs its own upgrades, and much web traffic still runs on pre-quantum schemes.

Adopting PQXDH and quantum-resistant PGP now is a way of closing the vault before the tools to open it are widely available.
