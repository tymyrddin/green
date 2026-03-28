# Handle research participant data

Research participant data carries a protection obligation that is both ethical and legal. The
people who provided it consented to a specific use in a specific context. Using it differently,
sharing it carelessly, or retaining it beyond the agreed period is not a minor administrative
lapse. It is a breach of the relationship that made the research possible.

This runbook covers the handling lifecycle: collection, storage, sharing, and deletion.

## Before collection

### Define what you actually need

Data minimisation applies more readily at the design stage than retrospectively. Before
building a data collection instrument, ask for each field: what decision or analysis does
this enable, and is that decision or analysis necessary for the research purpose?

Fields that are convenient to collect but not analytically necessary should be removed. A
participant's exact postcode enables fine-grained location analysis; if the research only
needs regional data, collect the region.

### Define consent precisely

Consent for research participation must be:
- Specific: what data will be collected, for what analysis, in what timeframe.
- Informed: in language the participant can actually understand, not legal boilerplate.
- Revocable: participants must be able to withdraw. What happens to their data if they do
  needs to be stated in advance.

Blanket consent to "future research purposes" does not satisfy GDPR requirements for specific
purpose. If you want to use data for a second study, you need a second consent process or a
clear statement in the original that the second use is within scope.

### Define retention and deletion

Before collection begins, specify: how long will the data be held, and what will trigger
deletion. Set a calendar reminder. Treating deletion as something to decide later is how
data outlives its consent.

## Collection and storage

### Pseudonymise at collection where possible

Separate identifying information from research data as early as possible. Assign each
participant a code. Keep the code-to-identity mapping in a separate system with stricter
access controls than the research data itself.

If the linking key is destroyed at the end of the study, the research data becomes genuinely
anonymised and is no longer subject to data protection obligations. Plan for this from the start.

### Encrypt

Research data should be encrypted at rest. Institutional network drives are not sufficient
on their own; add file-level or folder-level encryption for sensitive datasets.

### Restrict access

Only the researchers who need access to identifiable data should have it. Shared team drives
with broad access are common in academic environments and are a routine over-sharing risk.
Configure access to match need.

## Sharing data

### Within the research team

Use access controls, not email attachments. A dataset sent by email to a collaborator is a
dataset stored in an email inbox, potentially synced to a personal device, and possibly
forwarded somewhere else.

Share via a controlled system where access can be revoked. Log who has been given access.

### With external collaborators

Before sharing with anyone outside your institution, check:
- Does the consent cover sharing with this party?
- Is a data sharing agreement in place?
- What jurisdiction will the data be processed in? If outside the EU, is there a legal
  transfer mechanism?

Identifiable participant data should not be sent to a collaborator whose institutional cloud
storage sits under US jurisdiction without reviewing the legal transfer position. This is
not a hypothetical concern; it is a routine gap in cross-border collaboration.

### Publication

Anonymised or aggregated data can often be published or shared openly without consent
issues, provided the anonymisation is genuine. Test re-identification risk before publishing:
small group sizes, unusual combinations of attributes, and sparse datasets can allow
re-identification even without direct identifiers.

The playbooks in this collection include [data minimisation guidance](../playbooks/minimise.md)
relevant to this assessment.

## Deletion

At the end of the retention period, delete systematically:
- The research data itself.
- All backups of the research data.
- The consent records (after confirming legal retention obligations in your jurisdiction).
- Any copies shared with collaborators (confirm deletion with them).

Document that deletion occurred. If a regulatory authority ever asks why you no longer hold
the data, "we deleted it on schedule per our retention policy" is the answer you want to give.

If a participant has withdrawn consent and requested deletion mid-study, follow the same
process for their records specifically, as promptly as possible.
