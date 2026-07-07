# Account compromise response

Trigger: a login alert nobody initiated, a password reset email nobody requested, a notification of unrecognised account activity, or a contact reporting a message the account did not send.

Do not wait to see if it resolves itself. It will not.

## Secure the account immediately

If the account can still be logged into, change the password now, generating something new from a password manager. Do not reuse anything used before.

If the password has already been changed and locks the way out, go to the account recovery flow, using a recovery email or phone number the attacker does not control. If the recovery options themselves have been changed, contact the service's support team directly and report the compromise.

Once back in, revoke all active sessions, usually under Security or Devices in account settings. This logs out everyone currently connected, including the attacker.

## Assess what the account controls

An email account is a special case. If email was compromised, assume that any other account using it for login or password recovery is exposed too. Work through those in order of sensitivity and change their passwords.

For any account, review:
- What data was accessible from it?
- Were any actions taken during the compromise (emails sent, files accessed, settings changed)?
- Does it have admin access to other systems?

## Check for backdoors left behind

Attackers often set up persistence before leaving. Check for:
- New recovery email addresses or phone numbers.
- New authorised devices or sessions.
- OAuth applications granted access (under "Connected apps" or similar).
- Forwarding rules in email that silently copy everything sent.
- Profile changes that could feed a follow-on attack.

Remove anything that was not added deliberately.

## Enable or verify 2FA

If the account had no two-factor authentication, add it now (see the [authenticators runbook](../runbooks/authenticators.md)). If it had 2FA and was compromised anyway, check which recovery methods exist and whether the attacker used one of them, such as a SIM swap or access to a recovery email.

## Check adjacent accounts

Passwords get reused despite best intentions. If the compromised account's password appeared anywhere else, change every instance of it. Where it is unclear whether the account's contents included other stored passwords, treat every account sharing that password as compromised.

## Report and monitor

Report the compromise to the service. Most platforms have a dedicated route and may be able to explain how the access occurred.

Watch for follow-on activity over the following weeks: unusual login attempts elsewhere, unexpected messages from connected accounts, and social-engineering attempts against contacts using information the attacker now holds.
