# Audit what data you hold

A data audit answers the question: what personal or sensitive data does this organisation
actually hold, where is it, why is it there, and how long is it staying?

Most organisations have a partial answer to this at best. Data is created for one purpose
and retained long past it. Systems are connected to other systems and the data flows are
not tracked. A record that began as a live operational requirement becomes an archive that
becomes a liability.

The audit does not need to find everything in one pass. A first pass that covers the
highest-risk systems is more useful than a plan to cover everything that is never executed.

## Identify all systems holding data

Start with a list. Include:
- Databases and data stores (production, staging, analytics, backups)
- File storage (cloud drives, shared folders, local file servers)
- SaaS tools with data in them (CRM, HR, email, project management, customer support)
- Third-party processors (payroll providers, mailing list managers, analytics platforms)
- Email archives
- Paper records, if relevant

For each system, identify: who owns it, who administers it, and who has access.

## Classify what is in each system

For each system, identify the categories of data it holds:
- Personal data of customers or users (names, email addresses, behaviour data)
- Personal data of staff
- Sensitive special category data (health, political opinions, ethnicity, sexual orientation)
- Beneficiary or client data (for NGOs and service organisations)
- Research participant data
- Financial data
- Internal strategy or intellectual property

Note which categories have regulatory implications in your jurisdiction. In the EU, special
category data and children's data have stricter requirements.

## Document purpose and legal basis

For each category of data in each system, record:
- Why it was collected.
- What it is currently used for.
- The legal basis for holding it (consent, contract, legitimate interest, legal obligation).
- Whether the original purpose is still active.

Data held without a clear current purpose is a candidate for deletion. Data where the legal
basis has expired (for example, a customer relationship that ended three years ago) is likely
overdue for deletion.

## Check retention periods

Most organisations have a retention policy of some kind. The gap between the policy and what
is actually in the systems is usually large.

For each data category, ask: is there a defined retention period, and is it being applied in
practice? If not, set one and implement it. Data that is not needed should have a scheduled
deletion date, not an indefinite hold.

## Identify data to delete or archive

From the audit, you should have a set of data to act on:
- Data with no current purpose: delete.
- Data that must be retained for legal reasons but is no longer operationally needed: archive
  to secure, access-restricted cold storage. Remove from live systems.
- Data whose retention period has passed: delete, with documentation that the deletion occurred.

Deletion should be confirmed and documented. A deleted database backup that is not noted in
the audit record will appear as a gap on the next audit.

## Record and review

Document the audit: what was covered, what was found, what decisions were made, and when
the next review is scheduled.

A data audit is not a one-time exercise. The environment changes. New systems are added.
New data flows are created. Schedule a review annually, and review specifically when new
systems are added or significant changes are made to existing ones.

The audit record is also useful for regulatory compliance: if your supervisory authority
requests information about your data holdings, a maintained audit record demonstrates that
you are managing this deliberately rather than discovering it under pressure.
