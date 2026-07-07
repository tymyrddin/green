# Handle research participant data

Research participant data carries a protection obligation that is both ethical and legal. The people who provided it consented to a specific use in a specific context. Using it differently, sharing it carelessly, or retaining it beyond the agreed period breaks the relationship that made the research possible.

## Before collection

### Define what is actually needed

Data minimisation applies more readily at the design stage than retrospectively. Before building a collection instrument, ask of each field: what decision or analysis does it enable, and is that necessary for the research purpose?

Fields that are convenient but not analytically necessary are best removed. A participant's exact postcode enables fine-grained location analysis; where the research needs only regional data, collect the region.

### Define consent precisely

Consent for research participation has to be:
- Specific: what data will be collected, for what analysis, over what timeframe.
- Informed: in language the participant can actually understand, not legal boilerplate.
- Revocable: participants able to withdraw, with the fate of their data on withdrawal stated in advance.

Blanket consent to "future research purposes" does not satisfy GDPR's requirement for a specific purpose. A second study needs either a second consent process or a clear statement in the original that the second use is within scope.

### Define retention and deletion

Before collection begins, specify how long the data will be held and what will trigger deletion. Set a calendar reminder. Treating deletion as something to decide later is how data outlives its consent.

## Collection and storage

### Pseudonymise at collection where possible

Separate identifying information from research data as early as possible. Assign each participant a code, and keep the code-to-identity mapping in a separate system with stricter access controls than the research data itself.

Destroying the linking key at the end of the study makes the research data genuinely anonymised and no longer subject to data protection obligations. Plan for this from the start.

### Encrypt

Research data benefits from encryption at rest. Institutional network drives are not sufficient on their own; file-level or folder-level encryption covers sensitive datasets.

### Restrict access

Only the researchers who need identifiable data are the ones to have it. Shared team drives with broad access are common in academic environments and a routine over-sharing risk. Configure access to match need.

## Sharing data

### Within the research team

Use access controls, not email attachments. A dataset sent by email is a dataset in an inbox, potentially synced to a personal device, and possibly forwarded onward. Share through a controlled system where access can be revoked, and log who has been given access.

### With external collaborators

Before sharing beyond the institution, check:
- Does the consent cover sharing with this party?
- Is a data sharing agreement in place?
- Which jurisdiction will process the data? If outside the EU, is there a legal transfer mechanism?

Identifiable participant data is best not sent to a collaborator whose institutional cloud storage sits under US jurisdiction without first reviewing the legal transfer position. It is a routine gap in cross-border collaboration.

### Publication

Anonymised or aggregated data can often be published or shared openly without consent issues, provided the anonymisation is genuine. Test re-identification risk before publishing: small group sizes, unusual attribute combinations, and sparse datasets can allow re-identification even without direct identifiers. The [data minimisation guidance](../playbooks/minimise.md) in this collection is relevant to that assessment.

## Deletion

At the end of the retention period, delete systematically:
- The research data itself.
- All backups of it.
- The consent records, after confirming legal retention obligations in the jurisdiction.
- Any copies shared with collaborators, confirming deletion with them.

Document that deletion occurred. If a regulatory authority ever asks why the data is no longer held, "deleted on schedule per the retention policy" is the answer worth being able to give.

Where a participant withdraws consent and requests deletion mid-study, follow the same process for their records specifically, as promptly as possible.
