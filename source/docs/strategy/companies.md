# Companies

The most durable failure in corporate security is the belief that the organisation is unlikely
to be targeted. "We are not interesting enough" is a comfort, not an assessment. It is the mental
equivalent of leaving the greenhouse unlocked because the orchids inside are not famous.

The threat landscape facing companies combines all three models in this site: commercial data
extraction (which applies to their customer and employee data), nation-state surveillance (which
applies to their intellectual property, supply chains, and strategic plans), and in some contexts,
targeted abuse through individuals within the organisation.

The assets of a company are not only its systems. They are the mental representations
that drive decisions about what is worth protecting, who the adversaries are, how serious the risk
is, and what would constitute a sufficient response. Most breaches begin not with a sophisticated
exploit but with a gap between the security model and the actual environment.

## Where the model meets reality

### Data you hold and why

Every piece of data your organisation retains is a liability as well as an asset. Data collected
for one purpose will be used for others, either by your organisation or by whoever acquires it
through breach, legal process, or purchase.

Applying data minimisation at collection is harder than applying it retrospectively, but both
are possible and both reduce exposure. If you do not need detailed behavioural data on your
customers to provide your service, do not collect it. If you collected it under a prior model
of your business that no longer applies, delete it. The regulatory obligation under GDPR is
to collect only what is necessary and to retain it only as long as necessary. The security
obligation is the same, with a sharper edge.

### Access controls and the cost of broad permissions

The default direction in most organisations is toward accumulating access. Permissions are
granted and rarely reviewed. Accounts are not deprovisioned promptly when employees leave.
Service accounts accumulate privileges over time. Role boundaries blur under operational
pressure.

Each of these patterns is rational in the short term and produces accumulated risk. The
review of who has access to what is unglamorous work. It is also one of the most effective
things an organisation can do to reduce its blast radius when an account is compromised.

Access review should be treated as infrastructure maintenance, not a compliance exercise.
Infrastructure that is not maintained degrades. Access environments that are not reviewed
expand, and expansion is not neutral.

### Supply chain and vendor dependencies

A breach that enters through a vendor or service provider is not less damaging because you
did not introduce it directly. Third-party access is part of your attack surface, and the
security posture of the services you depend on affects your posture whether you assess it
or not.

The surveillance threat model identifies infrastructure dependency as a structural vulnerability:
organisations that have made themselves dependent on platforms they do not control have, in
effect, delegated a security decision to a party with different interests. That applies at
every scale, from small companies dependent on a single SaaS provider to large organisations
whose cloud architecture sits entirely in a foreign jurisdiction.

Vendor assessment is not a guarantee. It is a practice. Done regularly, it surfaces changes
in the supply chain before they become surprises.

## What prevents good security from being done

Organisations most often lose security arguments not because the rational case is weak but
because the conditions do not support change. A development team that has learned through
experience that security reviews mean delays and rarely catch problems that matter has formed
a view. That view determines behaviour more reliably than a policy. Changing the view requires
changing the experience, not issuing a better policy.

When the security team is experienced as an enforcement function that adds friction and issues
blame when things go wrong, information stops flowing to it. Incidents are managed locally.
Near-misses are not reported. The security team operates on a version of reality that the
organisation is careful not to disturb.

The alignment between what the organisation says about security and what it actually does is
not optional infrastructure. Security that appears in policy and disappears in practice is not
security. It is a story the organisation tells about itself. People inside the organisation
know the difference and adjust their behaviour accordingly.

## Incentives and accountability

Security investment is consistently underfunded relative to operational investment because
the benefits of security are invisible when it is working and the costs of security are
visible always. The people making budget decisions are responding to incentive structures
that reward visible delivery and have no mechanism for valuing the incidents that did not happen.

Before designing a security programme, identify what the organisation is currently rewarding.
If speed of release is rewarded and security reviews slow release, the system is rewarding the
bypass of security reviews. That does not change through a better security review process. It
changes through changes to the incentive structure.

Accountability for data breaches sits in a different place than accountability for the
practices that produce them. The CISO is accountable for the response. The product decisions
that retained unnecessary data, the IT decisions that allowed permission sprawl, and the
procurement decisions that chose a cheaper vendor with a weaker security posture are often
made by people with no accountability for the downstream consequences.

Clarifying ownership is not a cultural fix. It is a structural one. Who is accountable for
the security consequences of a product decision needs to be answered before the decision
is made, not after the breach.

## Playbooks

* [Minimise long-term data storage](../playbooks/minimise.md)
* [Keep anonymous data separate from your identity](../playbooks/identity.md)
* [Use a VPN](../playbooks/vpn.md)
* [Understand quantum-resistant encryption](../playbooks/quantum.md)
* [Run a periodic access review](../runbooks/access-review.md)
* [Audit what data you hold](../playbooks/data-audit.md)
* [Assess third-party vendor security](../playbooks/vendor-assessment.md)

## Runbooks

* [Respond to a suspected data breach](../runbooks/breach-response.md)
* [Vendor breach response](../runbooks/vendor-breach.md)
* [Responding to a legal demand for data](../runbooks/legal-demand.md)
* [Data subject request response](../runbooks/data-subject-request.md)
* [Phishing click response](../runbooks/phishing-response.md)
* [Account compromise response](../runbooks/account-compromise.md)
