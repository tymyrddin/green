# Account compromise response

Trigger: you received a login alert you did not initiate, a password reset email you did not
request, a notification of account activity you do not recognise, or someone tells you they
received a message from your account that you did not send.

Do not wait to see if it resolves itself. It will not.

## Secure the account immediately

If you can still log in, change the password now. Use your password manager to generate
something new. Do not reuse anything you have used before.

If you cannot log in because the password has been changed, go to the account recovery flow.
Use a recovery email address or phone number that the attacker does not control. If the
recovery options have been changed, contact the service's support team directly and report
the compromise.

Once back in: revoke all active sessions (usually under "Security" or "Devices" in account
settings). This logs out anyone currently logged in, including the attacker.

## Assess what the account controls

An email account is a special case. If it was your email, assume that any other account that
uses it for login or password recovery has been exposed. Work through those accounts in order
of sensitivity and change their passwords.

For any account, review:
- What data was accessible from it?
- Were there any actions taken during the period of compromise (emails sent, files accessed,
  settings changed)?
- Does this account have admin access to other systems?

## Check for backdoors left behind

Attackers often create persistence before leaving. Check for:
- New recovery email addresses or phone numbers added.
- New authorised devices or sessions.
- OAuth applications granted access (under "Connected apps" or similar).
- Forwarding rules set up in email that silently copy everything sent.
- Changes to your profile that could be used in follow-on attacks.

Remove anything you did not add.

## Enable or verify 2FA

If the account did not have two-factor authentication enabled, add it now. See the
[authenticators runbook](../runbooks/authenticators.md). If it did have 2FA but the
account was still compromised, check which recovery methods exist and whether the attacker
may have used one of them (SIM swap, recovery email access).

## Check adjacent accounts

Passwords are sometimes reused despite best intentions. If the compromised account had a
password that appeared anywhere else, change all instances of it.

If credentials from the breach may be available to the attacker (for example, you are
uncertain whether the account contents included passwords stored in the account), treat
all accounts with the same password as compromised.

## Report and monitor

Report the compromise to the service. Most platforms have a dedicated route for this and may
be able to tell you more about how the access occurred.

Monitor for follow-on activity over the next weeks: unusual login attempts on other accounts,
unexpected messages sent from accounts connected to this one, social engineering attempts
targeting your contacts using information the attacker now holds.
