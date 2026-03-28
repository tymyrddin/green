# After device seizure

Trigger: your device has been seized, confiscated, or taken out of your control by
authorities, at a border, or in any other circumstance where you could not prevent or
control access to it. This runbook covers what to do after the fact.

If you are preparing for a trip where seizure is possible, see the
[travel devices playbook](../playbooks/travel-devices.md) first.

## Assume the device is fully compromised

Regardless of what you were told about the purpose of the seizure, assume that everything
on the device has been copied and examined. This includes:
- All files and documents
- Browser history, cookies, and saved passwords
- Email and messaging application content
- App data and cached credentials
- Any accounts that were logged in

Do not use the device for sensitive activities again until you are confident it has not
been modified. A seized device may be returned with software installed on it that you
cannot detect through normal inspection.

## Notify your organisation

If this was a work device, notify your organisation's security team immediately. They
need to know what data was accessible from the device and may have their own notification
obligations if organisational or client data was involved.

## Change credentials for everything accessible from the device

Work through every account that was accessible, in order of sensitivity. For each:
- Change the password.
- Revoke all active sessions.
- Revoke any tokens, API keys, or OAuth connections that were configured on the device.
- Check account settings for changes made after the seizure (new recovery contacts,
  forwarding rules, authorised applications).

If you had a password manager logged in on the device, change the master password and
audit the vault for any accounts that were particularly sensitive.

## Assess data exposure for people whose data was on the device

If the device held personal data about clients, beneficiaries, research participants,
or other individuals, assess whether their exposure creates risks and whether you have
notification obligations. See the [breach response runbook](breach-response.md) for
the organisational response process.

For NGOs with beneficiaries in sensitive situations: consult your safety protocols and
your support organisation before taking any action that might alert the authorities who
conducted the seizure that you are responding.

## Handle the physical device

If the device is returned, do not return it to normal use immediately. Have it inspected
by a trusted technical person before using it for anything sensitive. If you cannot
confirm its integrity, treat it as permanently compromised and replace it.

If the device was not returned, follow your organisation's process for lost or stolen
devices. Report it to your insurance if relevant, and ensure your data audit reflects
the change in data holdings.

## Review what the seizure revealed

A device seizure is a signal that your threat model has escalated or was miscalibrated.
Review what data the device contained and whether it should have been there. If you were
carrying sensitive data that should have been on a clean travel device, update your
procedures for future travel.
