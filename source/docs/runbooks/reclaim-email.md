# Reclaim your primary email account

Your primary email is the root of your digital identity. Almost every other account can be reset through it, which means someone with access to your inbox can reach into your banking, social media, cloud storage, and anywhere else a password reset email lands. Securing it is the single most important digital step.

Do all of this from a device and network you trust. Not a shared device. Not the home Wi-Fi if the router was set up by the other person. A library computer, a trusted friend's phone, or a device purchased for this purpose are safer options.

## Change the password first

Use a long, unique passphrase that you have never used before and have not used anywhere the other person might know about. Do not use a variation of a previous password.

If you use a password manager, make sure the manager itself is on a device only you control and protected by a password the other person does not know. If the password manager was previously on a shared device or the other person had access to it, change the manager's master password from a safe device first.

## Check who else has access

Before adding new security, look at what access already exists.

In your email settings, look for:
- Forwarding rules that copy your incoming mail to another address
- Filters that delete, archive, or mark specific messages before you see them
- Delegated access or accounts that have permission to read or send as you
- Connected applications and OAuth grants that have access to your inbox
- Active sessions showing devices or locations that are not yours

Remove anything that should not be there. Forwarding rules are the most commonly abused: they can be set quietly and are easy to miss. A forwarding rule to the other person's address means they receive copies of every incoming email, including every verification code and password reset link, even after you change your password.

## Enable two-factor authentication

Once you have cleaned up existing access and changed the password, enable two-factor authentication using an authenticator app. Not SMS if you can avoid it: if the other person has any influence over your mobile account or a shared family plan, SMS codes can be intercepted.

Install an authenticator app (Aegis on Android, Raivo or Ente Auth on iOS) on a device only you control. Set up the 2FA, scan the QR code, and store the backup codes somewhere the other person cannot reach.

## Change your recovery options

Check what phone number and backup email address are registered as recovery options. These are the paths that bypass your password if you get locked out, and they are therefore also the paths an adversary can use to take over the account.

Replace the recovery phone number with a number the other person does not know. If you do not yet have a separate number, some email providers allow recovery via an authenticator app code instead. Replace the backup email address with one the other person does not have access to.

## Check account activity

Most email providers show a recent activity log. Look for logins from devices or locations you do not recognise, and for any account settings that were changed at times when you were not using the account.

If you see evidence of access you did not authorise, sign out all other sessions from the account settings. This terminates any active session the other person may still be using.

## After the email is secure

Once your email is secured, you can begin changing passwords on other accounts, because the recovery path for those accounts is now under your control. Start with your most sensitive accounts: banking and financial services, then the accounts you use most, then everything else.

See the [enable two-factor authentication](../playbooks/authenticators.md) playbook for rolling 2FA out more broadly, and the [audit shared accounts](../playbooks/audit-shared-accounts.md) playbook for working through the rest of the shared access picture.
