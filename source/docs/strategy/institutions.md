# Research and academic institutions

![Institutions](/_static/images/institutions.png)

Research institutions hold high-value assets under rules written for a lower-stakes age. They generate
intellectual property of genuine interest to state and commercial adversaries, host cross-border
collaborations that create jurisdictional complexity, and run governance frameworks designed before cloud
infrastructure and the modern commercial data layer, with IT departments under-resourced relative to the
value of what they protect. The mismatch is the threat model.

The assets at risk are not only research data. They include the identities of collaborators in sensitive
jurisdictions, the strategic content of unfunded proposals, the personal data of participants, and findings
whose value is highest before publication. The instinct that publication is the protection gets this
backwards: the most exposed window is the one before the work is public, and in some fields the unpublished
methods and data are worth more than the paper.

Data does not carry its protections across borders. A dataset held on a US-based service is subject to US
legal process wherever it originated, and for research involving human subjects that exposure can become a
harm the ethics review never weighed.

## From concern to action

| Concern | What can help |
| --- | --- |
| Pre-publication research or unpublished methods reaching a competitor | [Run a periodic access review](../runbooks/access-review.md), [audit what is held](../playbooks/data-audit.md) |
| Participant data crossing into a weaker jurisdiction, or kept past its purpose | [Handle research participant data](../runbooks/research-participant-data.md), [minimise what is kept](../playbooks/minimise.md), [separate identifiers from the records](../playbooks/identity.md) |
| A collaborator's device searched or seized at a border | [Prepare devices for travel](../playbooks/travel-devices.md), [what to do after a seizure](../runbooks/device-seizure.md) |
| Email and correspondence exposed | [Email privacy](../playbooks/email.md) |
| A cloud service or vendor the institution depends on | [Assess a vendor's security](../playbooks/vendor-assessment.md), [respond to a vendor breach](../runbooks/vendor-breach.md) |
| A legal demand, or a participant's data-subject request | [Responding to a legal demand](../runbooks/legal-demand.md), [handling a data-subject request](../runbooks/data-subject-request.md) |
| A breach of research or participant data | [Respond to a suspected breach](../runbooks/breach-response.md) |
| Data encrypted now, read once the cryptography breaks | [Quantum-resistant encryption](../playbooks/quantum.md) |

## The culture of openness and its costs

Academic culture is built on the premise that knowledge should be shared. Openness is a
professional value and in many fields an ethical one. This is good and worth preserving. It
is also in direct tension with the security posture required to protect sensitive research,
participant data, and collaborator identities.

Researchers who experience security controls as hostile to the culture of their field will
route around them. This is not a personal failing. It is a predictable response to a mismatch
between the way security is presented and the values that drive research behaviour.

The framing is the point. Security as protection of the research, the participants, and the
collaborators, rather than security as institutional risk management, is more likely to
be received as aligned with research values. It is also more accurate.

The cost of a breach in an academic context is significant and underweighted in institutional
planning. A research group whose unpublished findings are leaked to a competitor
experiences more than a data loss: a fundamental violation of the trust on which
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

Last reviewed: 2026-07-09.
