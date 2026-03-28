# Enable device encryption

An unencrypted device is a lost device that becomes a complete data breach. Full-disk
encryption means that without the correct passphrase or PIN, the data on the device
is unreadable, even if someone removes the storage and reads it directly.

Modern operating systems handle this transparently. You will not notice it is running.
What you will notice is that you need to enter your PIN or passphrase when the device
starts up, which is also when you would want that protection.

## MacOS (FileVault)

FileVault is Apple's full-disk encryption. On Macs with Apple Silicon or the T2 chip,
data is encrypted by default when a firmware password is set. On older hardware it requires
explicit enabling.

To check and enable:
1. System Settings > Privacy & Security > FileVault.
2. If it shows "FileVault is turned off," click Turn On.
3. You will be asked whether to allow your iCloud account to unlock the disk, or to create
   a recovery key. If your threat model includes anyone who could compel Apple to unlock
   your device via iCloud, choose the recovery key option. Store the key somewhere physically
   secure, not on the device.

## Windows (BitLocker)

BitLocker is available on Windows Pro, Enterprise, and Education editions. On Windows Home,
use VeraCrypt (see below).

To enable BitLocker:
1. Search for "Manage BitLocker" in the Start menu.
2. Click "Turn on BitLocker" on the drive you want to encrypt (usually C:).
3. When asked how to back up your recovery key, do not save it to your Microsoft account
   if you are concerned about cloud access. Save it to a file and store that file on a
   USB drive that you keep physically separate from the laptop.
4. Choose "Encrypt entire drive" rather than just the used space, particularly on an
   existing installation.

For Windows Home, download VeraCrypt from veracrypt.fr and use it to create a system
partition encryption. The process takes longer to set up but provides equivalent protection.

## Linux (LUKS)

LUKS (Linux Unified Key Setup) is the standard encryption layer for Linux. It is most
cleanly set up at install time: most major distributions (Ubuntu, Fedora, Debian) offer
full-disk encryption as an option during installation. Select it and set a strong passphrase.

If your system is already installed without encryption, the cleanest path is to back up
your data, reinstall with encryption enabled, and restore. Encrypting a running system
in place is possible but more complex.

## Mobile devices

iOS: iPhones are encrypted whenever a passcode is set. The encryption is hardware-backed
and tied to the device. Enable a passcode (a six-digit PIN minimum; an alphanumeric passphrase
is stronger) under Settings > Face ID & Passcode.

Android: Most modern Android devices encrypt by default when a screen lock is set.
To verify: Settings > Security > Encryption (path varies by manufacturer). If it shows
"Encrypted," you are done. If not, enable screen lock first and the encryption option
will appear.

## A note on biometrics at borders

Biometric unlock (fingerprint, face) is convenient and generally secure. At border crossings
or in situations where you may be compelled to unlock your device, a PIN or passphrase provides
more legal protection in many jurisdictions. Know your jurisdiction's rules before you travel.
The [travel devices playbook](travel-devices.md) covers this in more detail.
