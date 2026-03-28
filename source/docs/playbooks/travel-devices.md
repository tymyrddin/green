# Prepare devices for high-risk travel

Crossing a border with a device that contains sensitive data, communications, or credentials
is a different threat model from everyday use. Border agencies in many jurisdictions have
legal authority to inspect devices, compel passwords, and in some cases detain devices for
forensic imaging. This is not hypothetical: it has happened to journalists, researchers,
NGO staff, and lawyers travelling with sensitive materials.

The approach here is not to assume the worst at every border. It is to decide in advance
what your acceptable risk level is and prepare accordingly.

## Assess the trip

Before preparing anything, consider:
- What is the legal and political environment of the destination?
- What data are you carrying that, if exposed, would harm you, your organisation, or third parties?
- Are you on any list that would make targeted inspection more likely?
- Is the risk at the destination, at transit points, or at the border returning home?

The answers determine how much preparation is proportionate.

## Decide what goes with you

The cleanest option is a travel device: a laptop and phone that contain only what is needed
for the trip, with no access to sensitive accounts or data. This is not always practical, but
it is the most reliable approach.

If you are using your primary devices, before you leave:
- Back up everything to an encrypted location that stays home.
- Remove or log out of applications you do not need for the trip.
- Revoke access tokens for services you will not use (revoke OAuth connections, not just log out).
- Remove any sensitive files that are not needed. If you need them, consider whether they can
  be accessed from an encrypted remote location rather than stored locally.

Consider what a one-hour forensic imaging of your device would reveal to a motivated examiner.
If that is acceptable, proceed. If not, reduce further.

## Configure the devices

Disable biometric unlock before you approach the border. In many jurisdictions, a PIN or
passphrase has stronger legal protection than biometric unlock. An officer can observe your
face or take your finger; compelling you to disclose a passphrase has a higher legal bar in
many (not all) jurisdictions. Know the rules for where you are travelling.

Enable full-disk encryption if it is not already on. See [device encryption](../playbooks/device-encryption.md).

Set the device to lock immediately on sleep. Remove any persistent login tokens from browsers.

If you use a VPN, ensure it is configured and working before you leave. VPN services may
be blocked or illegal at the destination.

## Accounts and credentials

Log out of your password manager before approaching the border. Your credentials are of
limited use to an examiner who cannot access the vault.

If you need specific credentials during the trip, consider storing them in a note encrypted
separately rather than in a password manager that, once unlocked, reveals everything.

Change passwords for sensitive accounts before you leave if you have reason to believe the
trip is particularly high risk. Change them again when you return.

## At the border: what to expect and what to do

You will be asked to unlock your device. In most jurisdictions you are legally required to
comply. Refusing may result in device confiscation, entry denial, or in some jurisdictions,
arrest.

Know in advance what you will do if asked to unlock. If the answer is "comply," ensure the
device contains only what you are prepared to have examined. If the answer is "refuse," be
clear on the legal and practical consequences in that jurisdiction.

If your device is confiscated, note the time, who took it, and what you were told about the
process. Notify your organisation or legal contact as soon as possible.

## After return

Assume that any device that was out of your control, confiscated, imaged, or inspected should
be treated as potentially compromised.

Change passwords for any accounts that were accessible on the device. Revoke and reissue
API keys or tokens. If the device was a travel device, wipe it before using it for anything sensitive.

Review whether any data that was on the device should be considered exposed and whether this
triggers any notification obligations.
