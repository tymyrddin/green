# Research and academic institutions

Research institutions occupy an uncomfortable position in the surveillance landscape. They generate
intellectual property that is of genuine interest to state and commercial adversaries. They host
cross-border collaborations that create legal and jurisdictional complexity. They operate under
governance frameworks designed for an era before cloud infrastructure, before bulk collection, and
before the commercial data layer became as sophisticated as it is now. And they do most of this
with IT departments that are substantially under-resourced relative to the value of what they are
protecting.

The assets at risk are not only research data. They include the identities of collaborators in
sensitive jurisdictions, the strategic content of unfunded grant proposals, the personal data of
research participants, and in some fields, intellectual property with direct commercial or national
security implications. Each of these has different adversaries, different protection requirements,
and different failure modes.

## What the threat model actually looks like

### Intellectual property and pre-publication research

The surveillance threat model identifies economic and industrial intelligence as a distinct objective
for state-level actors. Research institutions are primary targets for this precisely because research
often has value before it is published. A competitor, state or commercial, that can access research
prior to publication avoids the costs of replication and may be able to use the findings before the
originating institution can.

The model that many institutions operate on is that publication is the protection: once the work is
public, the theft no longer matters. This model is wrong in two directions. First, the most valuable
window is pre-publication. Second, in some fields, the detailed methods, data, and non-published
findings may be more valuable than the published paper.

Infrastructure used for sensitive research should be treated as sensitive infrastructure. That means
network segmentation, restricted access, encryption at rest and in transit, and a clear policy on
what can be stored where and by whom.

### Cross-border collaboration

Academic collaboration crosses borders as a matter of practice. Collaborative work involving
researchers in countries with different legal frameworks, different intelligence relationships,
and different attitudes to intellectual property creates exposure that is difficult to manage
through technical controls alone.

The legal landscape is relevant. Data transferred to or processed in a jurisdiction outside
the EU may not be protected by GDPR equivalents. A collaborator who stores data on a US-based
cloud service subjects that data to US legal process regardless of where the data originated.
The researcher needs to understand this. The institution needs to have a policy that
acknowledges it.

For research involving human subjects, the stakes are higher. A dataset with identifiable
participant information that crosses into a jurisdiction with weaker protections or active
surveillance of the research topic creates harm potential that ethics review does not always
account for.

### Research participant data

The protection of research participants is an ethical requirement and, under most data protection
frameworks, a legal one. The practical implementation is often weaker than the governance
suggests.

Data collected from participants is frequently stored on institutional systems with broader
access than necessary, retained beyond the period required for the research, and shared with
collaborators without adequate attention to the consent boundaries.

Data minimisation, pseudonymisation where possible, and deletion when the retention period
expires are not novel requirements. They are routine practice that is routinely deferred. The
belief that institutional storage is secure enough to compensate for weak data hygiene is
contradicted repeatedly by the breach history of academic institutions.

## The culture of openness and its costs

Academic culture is built on the premise that knowledge should be shared. Openness is a
professional value and in many fields an ethical one. This is good and worth preserving. It
is also in direct tension with the security posture required to protect sensitive research,
participant data, and collaborator identities.

Researchers who experience security controls as hostile to the culture of their field will
route around them. This is not a personal failing. It is a predictable response to a mismatch
between the way security is presented and the values that drive research behaviour.

The framing matters. Security as protection of the research, the participants, and the
collaborators, rather than security as institutional risk management, is more likely to
be received as aligned with research values. It is also more accurate.

The cost of a breach in an academic context is significant and underweighted in institutional
planning. A research group whose unpublished findings are leaked to a competitor does not just
experience a data loss. It experiences a fundamental violation of the trust on which
collaboration depends. The damage to relationships, to future collaboration, and to individual
careers can be severe and lasting.

## Governance structures and their gaps

Academic governance is often diffuse. Responsibility for research data is distributed across
principal investigators, departments, IT, and central administration, with accountability
gaps at every junction. A dataset that no one owns fully is a dataset that no one protects
fully.

Clarifying ownership and accountability is experienced as a political act in flat or distributed
governance structures. It involves deciding who is responsible for decisions that currently
float, and floating responsibility is sometimes politically preferable to assigned responsibility
because it means no one can be held accountable.

The recurring pattern of inadequate data protection in academic research is not a symptom to
be fixed with a better training module. It is evidence that the governance model is wrong. That
model treats research data as primarily an administrative matter rather than a protection matter.
Correcting it requires changing what is treated as important, and that is a political as much as
a practical task.

Funders have more leverage here than they typically use. Research funding bodies that require
data management plans as a condition of grant approval could extend that to require security
plans for research involving sensitive data or cross-border collaboration. This is a structural
lever that does not depend on individual institutions to act first.

## Playbooks

* [Minimise long-term data storage](../playbooks/minimise.md)
* [Protect your email privacy](../playbooks/email.md)
* [Keep anonymous data separate from your identity](../playbooks/identity.md)
* [Understand quantum-resistant encryption](../playbooks/quantum.md)
* [Handle research participant data](../runbooks/research-participant-data.md)
* [Audit what data you hold](../playbooks/data-audit.md)
* [Prepare devices for high-risk travel](../playbooks/travel-devices.md)
* [Assess third-party vendor security](../playbooks/vendor-assessment.md)
* [Run a periodic access review](../runbooks/access-review.md)

## Runbooks

* [Respond to a suspected data breach](../runbooks/breach-response.md)
* [Responding to a legal demand for data](../runbooks/legal-demand.md)
* [Data subject request response](../runbooks/data-subject-request.md)
* [Vendor breach response](../runbooks/vendor-breach.md)
* [After device seizure](../runbooks/device-seizure.md)
