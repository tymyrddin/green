# Companies

![Companies](/_static/images/companies.png)

The most durable failure in corporate security is the belief that the organisation is unlikely
to be targeted. "We are not interesting enough" is a comfort, not an assessment. It is the mental
equivalent of leaving the greenhouse unlocked because the orchids inside are not famous.

A company's assets extend beyond its systems to the mental representations that drive
decisions about what is worth protecting, who the adversaries are, and what would count as a
sufficient response. Most breaches begin not with a sophisticated exploit but with a gap between
that model and the actual environment.

## From concern to action

| Concern                                                                    | What can help                                                                                                                                                               |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Customer or employee data kept longer than the use that justified it       | [Minimise what is collected](../playbooks/minimise.md), [separate identifiers from the records](../playbooks/identity.md), [audit what is held](../playbooks/data-audit.md) |
| Permission sprawl widening the blast radius when an account is compromised | [Run a periodic access review](../runbooks/access-review.md)                                                                                                                |
| A supplier or platform dependency becoming the way in                      | [Assess a vendor's security](../playbooks/vendor-assessment.md), [respond to a vendor breach](../runbooks/vendor-breach.md)                                                 |
| A staff member clicking a convincing phishing message                      | [Phishing click response](../runbooks/phishing-response.md)                                                                                                                 |
| An employee account taken over                                             | [Account compromise response](../runbooks/account-compromise.md)                                                                                                            |
| A breach of what the company holds                                         | [Respond to a suspected breach](../runbooks/breach-response.md)                                                                                                             |
| A legal demand, or a data-subject request under GDPR                       | [Responding to a legal demand](../runbooks/legal-demand.md), [handling a data-subject request](../runbooks/data-subject-request.md)                                         |
| Work data exposed on untrusted networks                                    | [Use a VPN](../playbooks/vpn.md)                                                                                                                                            |
| Data encrypted now, read once the cryptography breaks                      | [Quantum-resistant encryption](../playbooks/quantum.md)                                                                                                                     |

## Obstacles to good security

Organisations most often lose security arguments not because the rational case is weak but
because the conditions do not support change. A development team that has learned through
experience that security reviews mean delays and rarely catch problems that count has formed
a view. That view determines behaviour more reliably than a policy. Changing the view requires
changing the experience.

When the security team is experienced as an enforcement function that adds friction and issues
blame when things go wrong, information stops flowing to it. Incidents are managed locally.
Near-misses are not reported. The security team operates on a version of reality that the
organisation is careful not to disturb.

Security that appears in policy and disappears in practice is not security. It is a story
the organisation tells about itself. People inside the organisation
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

Clarifying ownership is a structural fix. Who is accountable for
the security consequences of a product decision needs to be answered before the decision
is made, not after the breach.

Last reviewed: 2026-07-09.
