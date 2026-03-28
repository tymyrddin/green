# Respond to a suspected data breach

A breach response that is invented during the crisis will be slower, more inconsistent, and
more likely to make things worse than one planned in advance. This runbook outlines the core
sequence. Read it before you need it. Adapt it to your organisation before you need it.

## Trigger conditions

This runbook applies when you have reason to believe that:
- An account has been compromised (unexpected login, unfamiliar activity, password reset you
  did not initiate).
- Data you hold has been accessed, exfiltrated, or exposed without authorisation.
- A system you operate has been compromised (ransomware, unexpected outbound traffic, alert
  from a security tool).
- A third party notifies you of a breach affecting your data.

"Reason to believe" does not require certainty. Investigate first, confirm later.

## Contain before you investigate

Before trying to understand what happened, reduce the ongoing damage:
- Revoke or rotate credentials for affected accounts.
- Isolate affected systems from the network if possible without destroying evidence.
- Suspend suspicious integrations or API keys.
- Do not delete logs or evidence. You will need them.

If you are not sure what is affected, contain broadly and narrow the scope as you investigate.

## Convene

Identify who is handling this. For small organisations, that may be one or two people. For
larger ones, it should be a defined group. Establish a communication channel for the response
team that is separate from the channels that may be compromised.

If you have an external incident response contact or a support organisation (Digital Defenders
Partnership, Access Now, Front Line Defenders for civil society; your cyber insurer or an IR
firm for companies), notify them now. Early notification costs nothing. Late notification
reduces what they can do.

## Assess scope

Work through the following:
- Which systems or accounts were affected?
- What data was accessible from those systems?
- What is the likely exposure window (from when to when)?
- How many people are affected?
- Is the attacker still active, or was this a one-time exfiltration?

Be precise about what you know versus what you are inferring. The scope assessment drives
everything that follows.

## Legal notification obligations

Under GDPR, if personal data has been breached, you must notify your supervisory authority
within 72 hours of becoming aware of the breach, unless the breach is unlikely to result in
a risk to individuals. The clock starts when you have reasonable certainty, not when you
begin investigating.

If individuals are at high risk from the breach, you must also notify them directly.

Document when you became aware, what you knew at that point, and what decisions you made. This
record matters if the authority later asks why it took the time it did.

For organisations in multiple jurisdictions, check the requirements for each. UK GDPR applies
to UK residents; EU GDPR applies to EU residents.

## Notify affected people

If individuals are at risk, tell them:
- What happened, in plain language.
- What data was involved.
- What risks they face as a result.
- What you have done and what they can do.

Do not send notification through a channel that may be compromised. Do not delay notification
to polish the language.

For NGOs holding beneficiary data: if disclosure to affected individuals would itself create
a safety risk, consult your support organisation before notifying. The obligation to notify
is real but so is the obligation not to put people in danger.

## Remediate

Once you understand the scope and have contained the immediate damage:
- Fix the vulnerability or misconfiguration that allowed the breach.
- Review adjacent systems for the same issue.
- Reset all credentials that may have been exposed, not just the ones you are certain were compromised.
- Restore from clean backups if systems were compromised.

## Post-incident review

After the immediate crisis, review what happened and why. The goal is not to assign blame
but to understand the conditions that produced the incident and whether they have been addressed.
Questions worth asking: Was the vulnerability known? Why had it not been fixed? Did detection
happen quickly enough? What would have helped?

Document the findings. Share them with relevant stakeholders. Act on them. The review that
produces no changes is not a review. It is a ritual.
