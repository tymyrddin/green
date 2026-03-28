# The L-space shelf

L-space connects all libraries. The shelves here are a selection of places worth returning to: organisations doing sustained work on digital rights and privacy, guides that are actively maintained, journalists and researchers who track the things that this site writes about. The list is short by design. A long list of links is a different thing from a useful shelf.

A note for anyone maintaining these pages: the sources in the investigative and research sections are also the most reliable for checking that the writing here reflects current conditions rather than conditions that obtained a year or two ago. The field moves quickly, and the pages in this repository need occasional review.


## Digital rights and policy

The Electronic Frontier Foundation publishes analysis, legal commentary, and practical guides on digital rights, surveillance, and the law as it applies to privacy. Their work covers both the technical and the legal dimensions, and their Deeplinks blog is worth following for developments that affect the tools and practices described here. The address is [eff.org](https://www.eff.org).

European Digital Rights, known as EDRi, is a network of civil society organisations across Europe working on digital rights, privacy, and online freedoms. Their collective monitoring of EU legislative developments, from the AI Act to chat control proposals, makes them the most useful single source for tracking how European law is changing in ways that affect the conditions this repository describes. The address is [edri.org](https://edri.org).

noyb, which stands for None Of Your Business, is the organisation founded by Max Schrems to bring strategic litigation under GDPR. Their complaints and rulings have produced some of the most significant enforcement actions in European data protection law, including the Schrems II decision that invalidated the EU-US Privacy Shield. Their published case summaries are directly relevant to the data broker and GDPR-deletion pages here. The address is [noyb.eu](https://noyb.eu).

La Quadrature du Net is a French digital rights organisation with particularly strong coverage of mass surveillance legislation, data retention, and state-level threats. Their analysis of French and European surveillance law is detailed and consistently well-sourced. The address is [laquadrature.net](https://www.laquadrature.net).

Access Now works on digital security and rights specifically for people at elevated risk: activists, journalists, and human rights defenders. Their Digital Security Helpline provides direct support, and their publications track policy developments across many jurisdictions. Their work is particularly relevant to the higher-risk scenarios that appear in the threat model pages. The address is [accessnow.org](https://www.accessnow.org).

Article 19 focuses on freedom of expression and information as human rights, with particular attention to surveillance and censorship. Their legal and policy analysis provides useful context for the pages here that cover state-level threats and censorship circumvention. The address is [article19.org](https://www.article19.org).

The Electronic Privacy Information Center, known as EPIC, is a US-based research and advocacy organisation focused on privacy law and emerging technology. Their publications cover regulatory developments and enforcement, which is relevant for the material on GDPR and data brokers. The address is [epic.org](https://epic.org).


## Practical guides

Privacy Guides at [privacyguides.org](https://www.privacyguides.org) maintains a carefully curated set of tool recommendations across all major categories: operating systems, browsers, messaging, email, VPNs, password managers, and more. The recommendations are community-maintained and updated regularly as tools change and new ones emerge. This is the most reliable single source for checking whether the specific tools mentioned in these pages are still current recommendations.

Surveillance Self-Defense, published by the EFF at [ssd.eff.org](https://ssd.eff.org), approaches privacy through a threat modelling lens. The guides are organised by context and risk level rather than by tool category, which aligns closely with the approach taken throughout this repository. The section on threat modelling is a useful companion to the threat model pages here.

Security in a Box, from Frontline Defenders at [securityinabox.org](https://securityinabox.org), is written specifically for civil society organisations and people working in environments with significant adversarial risk. The tool guides are practical and kept current. The framing is different from the household-level focus of the l-space pages, but the underlying principles are the same and the guides are a useful reference for the more technical material elsewhere in this repository.


## Investigative and journalistic sources

Forbidden Stories is a Paris-based consortium of investigative journalists whose model is to continue reporting stories that have been suppressed or whose authors have been silenced. They coordinated the Pegasus Project, which exposed the use of NSO Group's spyware against journalists, lawyers, and politicians across multiple countries, and the Predator Files, which documented the spread of commercial surveillance tools to authoritarian governments. Their investigations are the primary source of evidence for some of the more serious claims in the threat model pages here. The address is [forbiddenstories.org](https://forbiddenstories.org).

The Markup at [themarkup.org](https://themarkup.org) does data journalism on how technology actually behaves: how tracking works in practice, how algorithms affect real people, how platforms use the data they collect. Their investigations are well-sourced and typically include the technical detail needed to understand what they are describing. They are useful for validating claims about how tracking and data collection actually work, as distinct from how companies describe them in their privacy policies.

The Citizen Lab at the University of Toronto at [citizenlab.ca](https://citizenlab.ca) produces research on state-sponsored surveillance, spyware, and network interference. Their work is technically detailed and peer-reviewed, and it regularly surfaces new information about the tools and methods used by the adversaries that the threat model pages describe. Their publications are essential reading for keeping the higher-risk sections of this repository grounded in current evidence.

Bruce Schneier's Schneier on Security at [schneier.com](https://www.schneier.com) combines technical analysis with policy commentary and has maintained a high signal-to-noise ratio over many years. It is useful for tracking security developments that bear on the technical claims throughout this repository and for understanding how specific incidents fit into broader patterns.

Krebs on Security at [krebsonsecurity.com](https://krebsonsecurity.com) covers breaches, fraud, and criminal activity in the digital space with considerable technical depth. It is particularly useful for the pages covering data breaches, identity theft, and the practical consequences of poor credential hygiene.


## Technical standards and open research

The Open Observatory of Network Interference, known as OONI, measures internet censorship and network interference around the world. Their data and reports are publicly available at [ooni.org](https://ooni.org) and are relevant to the pages here that cover censorship, circumvention tools, and surveillance infrastructure at the national level. Their explorer tool allows you to look up conditions in specific countries, which is useful for grounding abstract threat descriptions in measured evidence.

The ENISA, the European Union Agency for Cybersecurity, publishes threat landscape reports, guidelines, and technical recommendations at [enisa.europa.eu](https://www.enisa.europa.eu). Their annual threat landscape report is a useful resource for checking that the threat descriptions here reflect the current state of play rather than the state of play at the time of writing.

Exodus Privacy is a French project that analyses the tracker libraries embedded in Android applications and publishes the results in a searchable database at [exodus-privacy.eu.org](https://exodus-privacy.eu.org). Their reports show which third-party trackers each app includes, what permissions it requests, and what network connections it makes. This is directly relevant to the stalkerware and surveillance pages: the same tracking infrastructure used by advertising networks appears in apps marketed as parental controls or productivity tools.

AlgorithmWatch is a Berlin-based research and advocacy organisation that investigates automated decision-making and algorithmic profiling as they affect people in practice. Their reports cover how profiling is used in employment, credit, public services, and law enforcement, grounding the more theoretical material in the inference and AI-profiling pages with documented examples from European contexts. The address is [algorithmwatch.org](https://algorithmwatch.org).

The Tor Project's blog at [blog.torproject.org](https://blog.torproject.org) covers developments in anonymity and censorship circumvention from the people who maintain one of the primary tools for it. It is relevant for the circumvention material and for understanding how the threat landscape affecting anonymity tools is changing, including adversarial attempts to de-anonymise Tor users.

The W3C Privacy Interest Group at [w3.org](https://www.w3.org/Privacy/) tracks how privacy is being designed into, or out of, the web platform. Their work is relevant for the browser-level tracking material here and for understanding what protections browsers can and cannot provide structurally, as distinct from what extensions and configuration choices can achieve on top of them.

The thinking behind the approach taken here is documented at [The Foundations](https://purple.tymyrddin.dev/docs/foundations/).
