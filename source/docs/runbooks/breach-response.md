# Respond to a suspected data breach

A breach response invented during the crisis will be slower, more inconsistent, and more likely to make things worse than one planned in advance.

## Trigger conditions

When there is reason to believe that:
- An account has been compromised (unexpected login, unfamiliar activity, an uninitiated password reset).
- Held data has been accessed, exfiltrated, or exposed without authorisation.
- An operated system has been compromised (ransomware, unexpected outbound traffic, a security-tool alert).
- A third party has notified a breach affecting the organisation's data.

"Reason to believe" does not require certainty. Investigate first, confirm later.

## Contain before investigating

Before working out what happened, reduce the ongoing damage:
- Revoke or rotate credentials for affected accounts.
- Isolate affected systems from the network where that is possible without destroying evidence.
- Suspend suspicious integrations or API keys.
- Do not delete logs or evidence; they will be needed.

Where the affected scope is unclear, contain broadly and narrow it during investigation.

## Convene

Identify who is handling the incident. For a small organisation that may be one or two people; for a larger one, a defined group. Establish a communication channel for the response team, separate from any channel that may itself be compromised.

Any external incident-response contact or support organisation (Digital Defenders Partnership, Access Now, Front Line Defenders for civil society; a cyber insurer or IR firm for companies) is worth notifying now. Early notification costs nothing; late notification reduces what they can do.

## Assess scope

Work through:
- Which systems or accounts were affected?
- What data was accessible from them?
- What is the likely exposure window, from when to when?
- How many people are affected?
- Is the attacker still active, or was this a one-time exfiltration?

Be precise about what is known versus inferred. The scope assessment drives everything that follows.

## Legal notification obligations

Under GDPR, where personal data has been breached, the organisation is required to notify its supervisory authority within 72 hours of becoming aware, unless the breach is unlikely to result in a risk to individuals. The clock starts at reasonable certainty, not at the start of investigation.

Where individuals are at high risk from the breach, the organisation has to notify them directly as well.

Document when awareness began, what was known at that point, and what decisions followed. That record is what an authority later weighs when asking why the response took the time it did.

For organisations spanning jurisdictions, check each: UK GDPR applies to UK residents, EU GDPR to EU residents.

## Notify affected people

Where individuals are at risk, tell them:
- What happened, in plain language.
- What data was involved.
- What risks follow from it.
- What has been done, and what they can do.

Do not send notification through a channel that may be compromised, and do not delay it to polish the language.

For NGOs holding beneficiary data: where disclosure to affected individuals would itself create a safety risk, consult a support organisation before notifying. The obligation to notify is real, and so is the obligation not to put people in danger.

## Remediate

Once the scope is understood and the immediate damage contained:
- Fix the vulnerability or misconfiguration that allowed the breach.
- Review adjacent systems for the same issue.
- Reset all credentials that may have been exposed, not only the ones known to be compromised.
- Restore from clean backups where systems were compromised.

## Post-incident review

After the immediate crisis, review what happened and why. The aim is not blame but understanding the conditions that produced the incident and whether they have been addressed. Worth asking: was the vulnerability known? Why had it not been fixed? Did detection happen quickly enough? What would have helped?

Document the findings, share them with the relevant stakeholders, and act on them. A review that produces no changes is not a review. It is a ritual.
