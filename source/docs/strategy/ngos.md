# NGOs and civil society

Organisations that work on human rights, environmental advocacy, political reform, or any area that
intersects with powerful interests face a threat landscape that differs from general commercial exposure.
The adversaries are not only data brokers. They include state intelligence services, law enforcement
with function-creep tendencies, private investigators retained by opponents, and in some jurisdictions,
criminal actors working at the instruction of state or corporate interests.

The assets at risk are not only organisational data. They include the people in your network: the
individuals who shared information, sought support, or participated in activities that could expose
them to retaliation. A breach that exposes a beneficiary list is not a data governance failure. It is
a harm to real people who trusted the organisation with their safety.

## What makes the threat model different

The [deanonymisation](../threat-models/deanonymisation/index.rst) and [surveillance](../threat-models/surveillance/index.rst)
threat models describe how data can be used to re-identify and
profile people. For civil society organisations, the attack surface includes those models plus
several others.

Organisations are targeted precisely because of their work. An adversary that cannot directly
observe an activist's communications may attempt to reach them through the organisations they
interact with. Donor records, beneficiary databases, internal strategy documents, and staff
communications are all potentially useful to adversaries with enough patience and access.

The legitimate appearance of the organisation can be used against it. A targeted NGO is not
necessarily compromised through a technical exploit. It may be compromised through a staff member
who receives a convincing phishing email appearing to come from a partner organisation, a funder,
or a journalist requesting comment.

Capacity is constrained. Most civil society organisations operate on budgets that do not allow
for dedicated security teams. The guidance that applies to a well-resourced technology company is
not automatically transferable. This is not a gap to apologise for. It is a constraint to design
around.

## Structural defences

### Compartmentalisation

Not everyone needs access to everything. Beneficiary data, donor data, internal strategy
discussions, and operational security information each have different sensitivity levels and
different consequences if exposed. Access should be structured to match need, not convenience.

The practical implementation of this is often resisted on grounds of friction or culture. The
friction is real. The alternative, a single breach that exposes everything because nothing was
segmented, is worse. Compartmentalisation does not require sophisticated tooling. It requires
deliberate decisions about who can see what, and follow-through in how systems are configured.

### Secure communications

Establish a baseline for internal communications: what is used for what, and why. Staff who are
uncertain which tool is appropriate for sensitive conversations will make inconsistent choices.
A policy that is explicit, brief, and actually followed is more useful than a comprehensive
framework that is ignored under time pressure.

For sensitive external communications, encrypted channels should be the default rather than the
exception. The person reaching out with a sensitive disclosure or request should not have to ask
for secure contact. It should be visible and easy.

For travel to high-risk jurisdictions, anticipate that devices may be subject to inspection or
seizure. Travel with clean devices where possible. Know in advance what you would do if a device
were confiscated.

### Beneficiary data

If you hold data about people who could face harm from its exposure, you have a protection
obligation that extends beyond regulatory compliance.

Minimise what you collect. The data you do not hold cannot be taken. If you do not need a
beneficiary's full name for the purpose at hand, do not record it. If you do not need location
data, do not collect it. If you need it temporarily, delete it when the need passes.

Where data must be held, encrypt it, restrict access to it, and plan for what happens if the
organisation is compelled by legal process to disclose it or is the subject of a breach.

### Incident response

Know what you will do before it happens. An organisation that discovers a breach during a crisis
and has to invent a response from scratch will make worse decisions than one that has thought
through the scenario in advance.

An incident response plan does not need to be long. It needs to answer: who decides what to do,
who communicates with whom, when do you tell affected people, and who can you call for help.
Digital Defenders Partnership, Access Now's Digital Security Helpline, and Front Line Defenders
all provide support to civil society organisations facing active threats.

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

Solidarity between organisations matters here. Shared threat intelligence, shared incident
response resources, and mutual support when an organisation is under attack are not just
nice-to-haves. They are structural defences against adversaries who benefit from civil society
operating in isolation.

The power asymmetry between the organisations described in the surveillance threat model and
most NGOs is real. Accepting that asymmetry as fixed is not required. Collective action at
regulatory and legislative level has reshaped data protection law before. That work continues.

## Playbooks

* [Use encrypted messaging](../playbooks/messaging.md)
* [Enable device encryption](../playbooks/device-encryption.md)
* [Protect your email privacy](../playbooks/email.md)
* [Minimise long-term data storage](../playbooks/minimise.md)
* [Keep anonymous data separate from your identity](../playbooks/identity.md)
* [Understand quantum-resistant encryption](../playbooks/quantum.md)
* [Prepare devices for high-risk travel](../playbooks/travel-devices.md)
* [Audit what data you hold](../playbooks/data-audit.md)
* [Assess third-party vendor security](../playbooks/vendor-assessment.md)
* [Detect stalkerware using PiRogue and Wazuh](../playbooks/pirogue-wazuh.md)
* [Monitor device traffic with a spare Android phone](../playbooks/pcapdroid.md)
* [Detect stalkerware using DNS monitoring](../playbooks/dns-detection.md)

## Runbooks

* [Respond to a suspected data breach](../runbooks/breach-response.md)
* [Suspected device compromise](../runbooks/device-compromise.md)
* [Doxxing response](../runbooks/doxxing-response.md)
* [Responding to a legal demand for data](../runbooks/legal-demand.md)
* [Vendor breach response](../runbooks/vendor-breach.md)
* [After device seizure](../runbooks/device-seizure.md)
