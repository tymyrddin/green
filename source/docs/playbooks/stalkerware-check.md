# Check a device for stalkerware

Stalkerware is software installed on a device to monitor it covertly: tracking location in real time, reading messages and emails, accessing the camera or microphone, logging keystrokes. It is often marketed as parental control or employee monitoring software. Its real use, in many cases, is surveillance of an intimate partner.

Read this page on a device you trust, not on the device you suspect is compromised.

## Before you check

Searching for stalkerware on a monitored device is itself visible to the monitoring software. If the device is compromised, the other person may see your search terms, the applications you open, and any scanning tool you install.

The safer first step is always to use a different device for sensitive activity. If you cannot be certain a device is clean, do not use it for communications you need to be private, for researching your situation, or for setting up new accounts.

Speak with a specialist support worker before running a scan if you can. The Coalition Against Stalkerware (stopstalkerware.org) lists vetted support organisations and tools. Decisions about when to scan, whether to remove detected software, and whether to reset the device depend on your overall safety situation, not only on what the scan finds.

## On Android

Stalkerware on Android requires the device to allow installation from outside the Play Store. Check whether this setting is enabled: Settings, then Security or Privacy, then Install unknown apps or Unknown sources. If it is on and you did not enable it, this is a signal worth taking seriously.

The Coalition Against Stalkerware recommends Malwarebytes (free, available on the Play Store) as a vetted scanner for Android. Install it, run a full scan, and review any flagged applications.

Also check manually: Settings, Apps or Application Manager, show all apps including system apps. Look for anything you do not recognise, particularly anything with a generic or plausible-sounding name and no obvious function. Note that stalkerware is often designed to hide itself, so a clean scan does not guarantee a clean device.

Check which apps have been granted unusual permissions: access to location, microphone, camera, contacts, and SMS. Go to Settings, Privacy, Permission Manager, and review each permission category for applications that should not have it.

## On iPhone

Apple's restrictions on third-party applications make traditional stalkerware harder to install on iPhones. The most common methods are either installing a Mobile Device Management (MDM) profile, which gives broad control over the device, or accessing iCloud from another device using the same credentials.

Check for MDM profiles: Settings, General, VPN and Device Management. Any profile installed there that you did not install yourself should be removed.

Check your Apple ID for devices signed in: Settings, your name at the top, scroll down to see all signed-in devices. Remove any you do not recognise.

Check iCloud access: if the other person has your Apple ID credentials, they can access your photos, messages (if backed up), and Find My location from their own device. Changing your Apple ID password and enabling two-factor authentication removes this access. See the [reclaim your primary email](../runbooks/reclaim-email.md) runbook for the approach to identity accounts generally; your Apple ID needs the same treatment.

Certo AntiSpy is a vetted tool that can check an iPhone for indicators of stalkerware when connected to a computer.

## The factory reset question

A factory reset is the most reliable way to remove stalkerware from a device. It is also the most disruptive, and it destroys potential evidence of the surveillance. This is a tradeoff that depends on your situation.

If you are considering legal action or already involved in proceedings, removing evidence by resetting the device may not be in your interest. If you need the device to be clean as quickly as possible, a reset may be the right choice.

A specialist support worker, or a solicitor familiar with technology-facilitated abuse, can help you make this decision with the full picture in view. Do not reset without thinking it through first.

## On-device firewall apps

On-device firewall apps can reveal unexpected background connections without requiring a separate monitor device. They work by inspecting traffic at the application level and showing you which apps are communicating with which remote hosts. This is less thorough than external traffic capture but requires no additional hardware.

On Android, NetGuard (free, available on F-Droid and the Play Store) works as a no-root firewall and traffic logger. It routes the device's traffic through a local VPN interface and shows per-app connections in real time. You can block individual apps from accessing the network entirely, which may interrupt stalkerware's ability to report home, and review the connection log to look for unexpected destinations.

On iPhone, Lockdown Privacy (free on the App Store) provides similar per-app traffic monitoring and blocking. It uses a local VPN in the same way as NetGuard and does not route your traffic through any external servers.

On Windows, GlassWire (free tier available) shows per-application network activity in a timeline view and alerts on new connections from applications that have not previously used the network.

The limitation of on-device tools is that sophisticated stalkerware may be able to detect or circumvent them, particularly on Android if it has obtained elevated permissions. They are more useful as a first check than as a definitive assessment. If you find suspicious connections, follow up with a scan using Malwarebytes (Android) or Certo AntiSpy (iPhone), and consider whether external traffic monitoring is warranted.

## After the device is clean

If you have confirmed or suspect the device was compromised, treat any account you accessed from it as potentially exposed. Change passwords for those accounts from a clean device. Check for new forwarding rules or connected apps in your email account. See the [audit shared accounts](audit-shared-accounts.md) playbook for working through the broader picture.
