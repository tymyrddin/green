# Vectors

Every greenhouse has multiple ways in. This one was built with most of them unlocked
from the inside.

## Legal vectors

The most important attack surface is not technical. It is legal. The
existence of legal access mechanisms means that the question is not "how do they get
in" but "under what conditions is the door already open".

National security exemptions remove the most significant legal barriers. A surveillance
activity conducted under a national security mandate operates outside GDPR entirely,
which means the data minimisation, purpose limitation, and consent requirements that
apply in commercial contexts simply do not apply here.

Secret court orders and intelligence warrants authorise targeted surveillance with
minimal transparency. In several EU jurisdictions, the subject of surveillance is
not informed, the details are classified, and oversight is exercised by a body that
cannot make its findings public. The legal process exists but operates in a way that
makes external challenge effectively impossible.

Cross-border legal instruments (MLATs, EU police and judicial cooperation frameworks)
make data accessible across borders through formal processes that are legitimate in
design but highly varied in practice. Data collected under one jurisdiction's legal
regime becomes accessible in another.

## Technical vectors

ISP and telecommunications interception: all EU telecom providers are required to
maintain lawful interception capability. This is infrastructure built into the network
that allows targeted or bulk interception of communications content and metadata.
The legal threshold for activating this capability varies by jurisdiction. The same
built-in access is a target in its own right: intrusions into telecom lawful-intercept
systems have shown that a capability built for authorised use is also a door others can force.

Backbone collection: signals intelligence agencies collect from undersea cables, internet
exchange points, and network infrastructure at points where large volumes of traffic
can be accessed at once. This collection captures data transiting a jurisdiction
regardless of where it originates or terminates. The legal framework for backbone
collection is generally less restrictive than for targeted individual interception.

Device and software compromise: mercenary spyware such as NSO's Pegasus or Paragon's
Graphite can compromise a device and read everything on it, including encrypted
communications, in current cases through zero-click exploits that need no action by the
target. It is used against high-value targets and has been documented against EU
politicians, journalists and lawyers; the [Paragon case](cases/paragon.md) is the recent,
forensically confirmed instance.

On-device scanning: a newer, still-contested vector would place inspection on the device
itself. Proposals to scan message content against a database before it is encrypted, the
mechanism behind the EU's [Chat Control](landscape/scanning-and-encryption.md) debate, would
turn every participating phone into a checkpoint, reaching content that transport encryption
would otherwise protect.

## Platform vectors

Technology platforms hold communications, social graph data, location history, and
behavioural profiles for enormous numbers of people. Legal instruments (national
security letters, court orders, formal cooperation requests) can compel platforms
to provide this data. In some cases, platforms cooperate informally or maintain
technical backdoors under classified arrangements.

Platforms hosted on non-EU infrastructure present a jurisdictional complication: the
data may be subject to the legal regime of the hosting country (most commonly the
United States) as well as to the EU regime. US intelligence agencies can access
data held by US-incorporated companies through instruments including Section 702 of
the Foreign Intelligence Surveillance Act and Executive Order 12333, and the US CLOUD Act
lets US authorities compel a US-based provider to hand over data it controls wherever in
the world it is stored, regardless of where the data was generated or who generated it.

This is the direct practical consequence of European dependency on US cloud
infrastructure. The transfer arrangement between the EU and US, currently the EU-US Data
Privacy Framework, is the third attempt after Schrems I struck down Safe Harbor in 2015 and
Schrems II struck down Privacy Shield in 2020, and it is [itself under
challenge](landscape/cross-border-transfers.md). It operates under the same structural
tension that invalidated its predecessors: US national security law applies to US companies
regardless of what a bilateral agreement says.

## Commercial vectors

Data brokers aggregate and sell information that would otherwise require legal
instruments to collect. Location data, behavioural profiles, social connections, and
identity information purchased from brokers is acquired commercially, not through
interception. No warrant is required. No target needs to be named. The purchase is
a commercial transaction.

The advertising technology ecosystem generates surveillance-grade data as a byproduct
of serving advertisements. Location data, device identifiers, browsing history, and
app usage patterns flow through ad-tech pipes at scale. This data is commercially
available to any buyer with a budget, including government agencies and their
contracted intermediaries, as the [Databroker Files](cases/databroker-files.md) investigation
of 2025 demonstrated inside the EU's own institutions.

## Structural vectors

Infrastructure dependency: European digital infrastructure is heavily reliant on
non-EU platforms, cloud services, and hardware manufacturers. Data processed on
foreign infrastructure is subject to foreign legal jurisdiction regardless of where
the data subject lives. This is not a targeted attack vector. It is a structural
condition that creates permanent jurisdictional leakage.

State database interoperability: the EU's border and security databases (the Entry/Exit
System, Eurodac, the Schengen and Visa Information Systems) are being connected into a shared
biometric search layer, described in the [legal landscape](landscape/biometric-and-border.md).
Interoperability is less an intrusion than a change of scale: data gathered for one purpose
becomes queryable alongside everything else, and joinability is itself a capability.

Vendor supply chain: telecommunications equipment from vendors with contested
relationships to foreign governments (the most discussed example being Huawei),
software with undisclosed telemetry, and hardware with firmware that may have been
modified create collection opportunities that do not depend on legal process.
The supply chain vector affects not just individual devices but network architecture.

Last reviewed: 2026-07-16.
