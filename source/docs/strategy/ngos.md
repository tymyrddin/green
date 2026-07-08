# NGOs and civil society

![NGO's](/_static/images/ngos.png)

An organisation that contests power inherits the adversaries of the powerful. The assets at risk are not
only organisational data; they are the people in the network, the individuals who shared information, sought
support, or took part in activities that could expose them to retaliation. A breach that exposes a beneficiary
list is not a data governance failure. It is a harm to real people who trusted the organisation with their
safety.

The organisation is also the route to them. An adversary who cannot reach an activist directly may reach them
through the organisations they deal with, often not through a technical exploit but through a staff member who
opens a convincing message appearing to come from a partner, a funder, or a journalist. Capacity is
constrained as well: most civil society organisations run on budgets that do not stretch to a security team,
so guidance written for a well-resourced company does not transfer. That is not a gap to apologise for. It is
a constraint to design around.

## From concern to action

| Concern                                                                                | What can help                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A beneficiary or donor list becoming a harm to the people who trusted the organisation | [Minimise what is collected](../playbooks/minimise.md), [keep names separate from the data](../playbooks/identity.md), [audit what is held](../playbooks/data-audit.md)                                                                       |
| Internal or external communications read by an adversary                               | [Encrypted messaging](../playbooks/messaging.md), [email privacy](../playbooks/email.md), [device encryption](../runbooks/device-encryption.md)                                                                                               |
| Devices searched or seized crossing into a hostile jurisdiction                        | [Prepare devices for travel](../playbooks/travel-devices.md), [what to do after a seizure](../runbooks/device-seizure.md)                                                                                                                     |
| A staff device suspected of being monitored                                            | [PiRogue and Wazuh](../playbooks/pirogue-wazuh.md), [a spare Android as a traffic monitor](../playbooks/pcapdroid.md), [DNS-level detection](../playbooks/dns-detection.md), [suspected device compromise](../playbooks/device-compromise.md) |
| A supplier or platform the organisation depends on becoming the way in                 | [Assess a vendor's security](../playbooks/vendor-assessment.md), [respond to a vendor breach](../runbooks/vendor-breach.md)                                                                                                                   |
| A legal or state demand for the data held                                              | [Responding to a legal demand](../runbooks/legal-demand.md)                                                                                                                                                                                   |
| A breach exposing what the organisation holds                                          | [Respond to a suspected breach](../runbooks/breach-response.md)                                                                                                                                                                               |
| A staff member or someone in the network doxxed                                        | [Doxxing response](../runbooks/doxxing-response.md)                                                                                                                                                                                           |
| Data encrypted now, read once the cryptography breaks                                  | [Quantum-resistant encryption](../playbooks/quantum.md)                                                                                                                                                                                       |

## Culture under pressure

Organisations that work in difficult contexts often develop security cultures that are either
overly informal (we trust each other, we do not need formal controls) or overly anxious (every
conversation is a potential leak). Neither is accurate, and both produce bad outcomes.

The informal model underestimates how often targeted attacks come through trusted channels. The
adversary does not usually announce themselves. The anxious model makes communication harder and
can suppress the honesty and information flow that effective organisations depend on.

People under stress communicate differently, and security cultures feel this before incident logs
do. When staff feel that a security conversation will result in blame or burden rather than
support, they will manage disclosures carefully. Near-misses will not be reported. Incidents will
be minimised. The security culture will become incongruent with the actual state of the organisation.

Building a culture where security incidents are reported without fear requires that reporting
be experienced as useful rather than punishing. Respond to disclosures with problem-solving,
not interrogation. Treat someone who reports a phishing click as someone who helped you find
a gap, not someone who created a problem.

## The structural conditions

Civil society organisations are targeted partly because they contest power. The same political
conditions that make their work necessary also make them adversarial targets for actors with
resources and institutional access that most NGOs cannot match.

This is not defeatism. It is a calibration. The goal is not perfect security. The goal is
raising the cost and complexity of surveillance sufficiently that casual or speculative
targeting becomes less rewarding, and that if targeted attacks do occur, the damage is
contained.

Solidarity between organisations is what does the work here. Shared threat intelligence, shared incident
response resources, and mutual support when an organisation is under attack are not just
nice-to-haves. They are structural defences against adversaries who benefit from civil society
operating in isolation. Digital Defenders Partnership, Access Now's Digital Security Helpline,
and Front Line Defenders all support organisations facing active threats.

The power asymmetry between the organisations described in the surveillance threat model and
most NGOs is real. Accepting that asymmetry as fixed is not required. Collective action at
regulatory and legislative level has reshaped data protection law before. That work continues.
