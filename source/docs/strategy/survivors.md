# Survivors of partner abuse

This page is different from the others in this section. Most defensive strategies assume an adversary who is largely unknown, operating from outside. Here the adversary knows you well, may have had fully legitimate access to your accounts and devices, and may still have access you are not aware of. The threat is intimate, which changes almost everything about how to respond.

If any part of this applies to your situation, you are not overreacting. The [poweron threat model](../threat-models/poweron/index.rst) describes in detail how technology-facilitated abuse works and what the patterns look like. This page is about what to do with that understanding.

Before anything else: specialist support organisations have advisors who understand this situation and can help you sequence your response safely. The digital steps here do not replace that. They sit alongside it.

## What makes this threat model different

In most security contexts, the goal is to keep an outsider out. Here, the problem is more complicated: access was often granted during a relationship that has changed. The person who helped set up your phone, who knew your PIN because you trusted them, who shares a family plan or a streaming account, is not an outside attacker. They are someone who accumulated access over time and may still hold it.

This means the standard advice, change your passwords, enable two-factor authentication, applies, but it does not apply in the usual order or in the usual way. Changing a password on an account the other person is actively watching may alert them before you are ready. Securing your email is the most important step, but doing it incorrectly can lock you out of your own recovery options.

The [attacks page](../threat-models/poweron/attacks.md) in the poweron model describes the recurring patterns: access that was never revoked, recovery-chain control, ambient surveillance, narrative manipulation. Understanding which patterns are present in your situation helps you prioritise what to address first.

## Safety before security

Some digital steps carry risk if taken at the wrong moment. An abuser who notices their location access has been removed, or that their device session has been logged out, or that an account they were monitoring has changed its password, may escalate. The digital response needs to be sequenced against a broader plan for physical safety.

This is the single most important thing to do before any digital steps: speak with a specialist organisation. They will not judge. They understand the technology. They can help you think through what order makes sense for your specific situation.

In the UK, Refuge and Women's Aid both have specialists in technology-facilitated abuse. The Safety Net project at the National Network to End Domestic Violence has detailed guidance. The Coalition Against Stalkerware connects survivors with vetted technical support.

Use a device the other person cannot access for any research or planning, including reading this page. A library computer, a trusted friend's phone, or a device purchased for this purpose are all options. Do not search on a device that may be monitored.

## The identity anchor: email first

Your primary email account is the root of your digital identity. Password resets, verification codes, and account recovery for almost every other service route through it. If someone has access to your email, or has set up forwarding rules within it, they can intercept recovery flows and reach into other accounts without needing the passwords to those accounts.

The [reclaiming your primary email](../runbooks/reclaim-email.md) runbook covers the steps in order: securing the password, enabling two-factor authentication, checking for forwarding rules and connected applications, reviewing active sessions, and changing the recovery options. Do this from a device you trust and a network you trust. Do not do it on a shared device or a home network that the other person controls.

Once the email is secured, the rest follows more safely, because the root of the recovery chain is no longer accessible to them.

## Shared access and surveillance

Technology used during a relationship accumulates shared access that is not always visible. Apple Family Sharing, Google Family accounts, shared streaming services, cloud storage with shared folders, smart home applications, location sharing features: each of these may currently provide visibility into your location, activity, or communications. None of it looks unusual because it was all set up normally.

The [audit shared accounts](../playbooks/audit-shared-accounts.md) playbook works through the main categories systematically. The goal is not to remove everything at once, but to understand what currently exists and to make deliberate choices about what to close and when, in the order that fits your safety situation.

Stalkerware, purpose-built software designed to run invisibly on a device, is a separate problem. It cannot always be detected by normal inspection. The [check a device for stalkerware](../playbooks/stalkerware-check.md) playbook covers how to approach this carefully, but the short version is: if you suspect a device is compromised, do not use it for any sensitive activity. The most reliable response is a factory reset, but this removes evidence. A specialist support worker can help you think through that tradeoff before acting.

## The physical environment

Smart home devices, if the other person has administrator access, can control your locks, lights, thermostat, and cameras. They can also log presence and routine. If you live somewhere with smart home devices installed during the relationship, assume they are still accessible. The smart home application on the other person's phone continues to work until access is deliberately removed, and removing it from a shared account requires knowing who has administrator access.

Bluetooth trackers, hidden in cars, bags, or belongings, are small and easy to overlook. If you suspect a tracker has been placed, the Apple AirTag detection feature (built into iPhones and available as a separate Android application) and Tile detection tools can locate them. Carry a physical sweep through your belongings and vehicle.

## Reputation and fabricated evidence

Digital evidence can be manipulated. Screenshots can be edited. AI tools can generate convincing audio, images, and video attributed to you. This is not hypothetical; it is described in the [attacks page](../threat-models/poweron/attacks.md) and it is occurring in legal proceedings and in reports to employers, schools, and social services with increasing frequency.

Preserving evidence of the genuine situation matters, but so does not conducting that preservation on a compromised device. Use a safe device to document what is happening: screenshots with timestamps, records of contacts, evidence of access and surveillance. Do not delete anything that may be relevant, even if it is distressing to keep. Legal and support workers can help you understand what matters and how to present it.

## Financial independence

Financial control is a form of abuse. Shared bank accounts, credit products taken out in your name, buy-now-pay-later accounts opened without your knowledge, and subscriptions billed to your card are all mechanisms through which financial monitoring and interference operate.

Contact your bank from a safe device, not from one that may be monitored. Most banks have trained staff who understand domestic abuse situations and can help you understand what access currently exists and how to separate it. Check for accounts you did not open. Check for authorised access on your existing accounts. If your income comes through a shared account, understand what steps are needed to redirect it before taking any visible action.

## The longer view

Reclaiming your digital life after technology-facilitated abuse takes time. It is not a single afternoon's work. Identity infrastructure takes time to rebuild. Trust in your own devices and connections takes time to restore. Some impacts, particularly if fabricated content has been distributed or false reports made, have timelines that depend on institutions and platforms, not only on your own actions.

This is not a failure of the process. It is the nature of the problem. Each step forward, securing the email, auditing the shared accounts, getting a clean device, understanding the financial position, is a meaningful reduction in the other person's reach. Doing it in the right order, with support, is more important than doing it quickly.

## Playbooks

* [Reclaim your primary email account](../runbooks/reclaim-email.md)
* [Audit and revoke shared account access](../playbooks/audit-shared-accounts.md)
* [Check a device for stalkerware](../playbooks/stalkerware-check.md)
* [Detect stalkerware using PiRogue and Wazuh](../playbooks/pirogue-wazuh.md)
* [Monitor device traffic with a spare Android phone](../playbooks/pcapdroid.md)
* [Detect stalkerware using DNS monitoring](../playbooks/dns-detection.md)
* [Set up a password manager](../runbooks/passwords.md)
* [Enable two-factor authentication](../runbooks/authenticators.md)
* [Use encrypted messaging](../playbooks/messaging.md)
* [Enable device encryption](../runbooks/device-encryption.md)
* [Keep anonymous data separate from your identity](../playbooks/identity.md)
* [Remove yourself from data broker sites](../playbooks/brokers.md)
* [Strip metadata from photos](../runbooks/photos.md)
* [Prepare a device for a situation where it may be seized or searched](../playbooks/travel-devices.md)

## Playbooks

* [Digital safety steps when leaving](../playbooks/leaving-safely.md)
* [Suspected device compromise](../playbooks/device-compromise.md)

## Runbooks

* [Account compromise response](../runbooks/account-compromise.md)
* [Doxxing response](../runbooks/doxxing-response.md)
* [After device seizure](../runbooks/device-seizure.md)
