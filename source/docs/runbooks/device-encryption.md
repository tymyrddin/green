# Enable device encryption

An unencrypted device is a lost device that becomes a complete data breach. Full-disk encryption means that without the correct passphrase or PIN, the data on the device is unreadable, even to someone who removes the storage and reads it directly.

Modern operating systems handle this transparently. It runs unnoticed. The one visible effect is entering a PIN or passphrase when the device starts up, which is exactly when that protection is wanted.

## MacOS (FileVault)

FileVault is Apple's full-disk encryption. On Macs with Apple Silicon or the T2 chip, data is encrypted by default once a firmware password is set. Older hardware needs it enabled explicitly.

To check and enable:
1. System Settings, Privacy and Security, FileVault.
2. If it shows "FileVault is turned off", click Turn On.
3. The setup asks whether to let an iCloud account unlock the disk, or to create a recovery key. Where the threat model includes anyone who could compel Apple to unlock the device via iCloud, choose the recovery key. Store it somewhere physically secure, not on the device.

## Windows (BitLocker)

BitLocker is available on Windows Pro, Enterprise and Education editions. On Windows Home, VeraCrypt covers the same ground (below).

To enable BitLocker:
1. Search for "Manage BitLocker" in the Start menu.
2. Click "Turn on BitLocker" on the drive to encrypt (usually C:).
3. When asked where to back up the recovery key, avoid the Microsoft account where cloud access is a concern. Save it to a file on a USB drive kept physically separate from the laptop.
4. Choose "Encrypt entire drive" rather than only the used space, particularly on an existing installation.

For Windows Home, VeraCrypt from veracrypt.fr can create system-partition encryption. It takes longer to set up but provides equivalent protection.

## Linux (LUKS)

LUKS (Linux Unified Key Setup) is the standard encryption layer for Linux. It is cleanest to set up at install time: most major distributions (Ubuntu, Fedora, Debian) offer full-disk encryption as an installation option. Select it and set a strong passphrase.

For a system already installed without encryption, the cleanest path is to back up the data, reinstall with encryption enabled, and restore. Encrypting a running system in place is possible but more involved.

## Mobile devices

iOS: iPhones are encrypted whenever a passcode is set. The encryption is hardware-backed and tied to the device. Set a passcode under Settings, Face ID and Passcode (a six-digit PIN at minimum; an alphanumeric passphrase is stronger).

Android: most modern Android devices encrypt by default once a screen lock is set. To verify, Settings, Security, Encryption (the path varies by manufacturer). An "Encrypted" status means it is done; otherwise, enabling a screen lock first makes the encryption option appear.

## A note on biometrics at borders

Biometric unlock (fingerprint, face) is convenient and generally secure. At border crossings, or anywhere unlocking may be compelled, a PIN or passphrase carries more legal protection in many jurisdictions. The rules are worth knowing before travelling. The [travel devices playbook](../playbooks/travel-devices.md) covers this in more detail.
