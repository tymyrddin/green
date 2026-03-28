# Assess third-party vendor security

Every vendor or service provider with access to your systems or data is part of your attack
surface. A breach that enters through a vendor is not less damaging because you did not
introduce it. The relevant question is not whether you trust the vendor, but whether their
security posture is adequate for the access they have.

Run this assessment before onboarding a new vendor with data access, and repeat it at
contract renewal.

## Define the access and data scope

Before assessing the vendor, be clear about what they will access:
- What systems will they connect to?
- What categories of data will they process or store?
- Where will that data be processed (jurisdiction)?
- Will they have human access or only automated/API access?
- What would be the impact if their access were compromised?

This scope determines how thorough the assessment needs to be. A vendor that will only
receive anonymised usage statistics warrants less scrutiny than one that will hold
customer personal data or have admin access to core infrastructure.

## Review documentation

Request or review the following from the vendor:
- Security certifications: ISO 27001, SOC 2 Type II, or equivalent. A SOC 2 report covers
  the controls in place; a Type II report covers whether those controls are operating
  effectively over time. Prefer Type II.
- Penetration test summary or report (within the last 12 months).
- Data processing agreement (DPA), required under GDPR for any vendor processing personal
  data on your behalf. If they cannot provide one, they cannot process EU personal data
  lawfully.
- Breach history: have they had incidents? How did they respond? Transparency here is a good
  sign. Evasiveness is not.
- Subprocessor list: who do they in turn share data with, and where?

## Ask the questions they will not volunteer

Standard vendor questionnaires exist (SIG, VSA, CAIQ for cloud providers). Use one if you
have one, or cover these areas:

- How is data encrypted at rest and in transit?
- How is access to the data controlled internally? Who at the vendor can access your data?
- What is their incident response process and how quickly would they notify you of a breach?
- How do they handle data at end of contract? What is the deletion process and timeline?
- What security training do their staff receive?
- How do they manage third-party access to their own systems?

Assess the answers for specificity. "We take security seriously" is not an answer.
"We encrypt at rest using AES-256, access is logged and reviewed quarterly, and we will
notify within 24 hours" is an answer.

## Review the contract

The security assessment is only as useful as the contractual protections that back it up:
- Does the contract include a DPA with the required GDPR clauses?
- Does it specify security requirements and give you audit rights?
- Does it require notification of breaches within a defined timeframe?
- Does it specify data deletion on termination and what "deletion" means?
- Does it allow you to terminate if the vendor has a serious incident?

If the standard contract does not include these, negotiate them in. Many vendors have a
security addendum. Ask for it.

## Ongoing monitoring

The assessment at onboarding captures the vendor's posture at one point in time. Things change.

- Monitor vendor security announcements and breach disclosures. Most significant vendors
  have security bulletins or CVE disclosures.
- Repeat the full assessment at contract renewal.
- Review access permissions annually and revoke anything not actively needed.
- If the vendor is acquired or merges, re-assess. Security posture and contractual
  commitments do not automatically transfer.
