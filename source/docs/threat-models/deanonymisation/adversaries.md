# Adversaries

Every well-tended garden has uninvited guests. Some chew at the edges, some uproot the hard work entirely, and others simply trample through with a clipboard and bad intentions. In the digital greenery of a life, these are the people rooting around the personal data in it, intentionally or not.

## Data scientists

Not all adversaries come in hoodies; some wear lanyards and call it "insight". Armed with Python and plausible deniability, and with access to mountains of data, data scientists build models that deanonymise individuals faster than anyone can say "training set". The tells are familiar: linking datasets that were "totally anonymised, promise", spotting the patterns in how a person walks, types or browses, and blaming the algorithm when the results turn creepy.

## Advertising ecosystems

The hydra of the browsing history. Online ads are not just about persuading anyone to buy trainers; behind the banners sits a vast network of trackers, bidders, data sharers and quiet observers, and clicks are the currency. Real-time bidding leaks metadata faster than a gossiping robin, behavioural profiles are built from innocent-seeming interactions, and the tracking does not wait for a click, since just loading the page is enough.

## Data brokers

A life, sliced, diced and monetised. Data brokers love a messy garden: they hoover up the trails people never knew they left, the searches, purchases, movements and moods, and sell them to anyone with a budget. The trade is matching online habits to an offline identity, packaging and reselling the result to just about everyone, and operating in the legal shadows behind opt-out systems no one can find.

## Face-search services

A photograph turned into a name. Firms such as Clearview AI and PimEyes scrape billions of images from the open web and social media and offer a search that runs a face against the lot, so a single photo becomes an identity, a home address, a set of associations. The customers range from law enforcement to anyone who pays, and European data-protection authorities have fined the largest of them repeatedly, so far without much changing.

## Automated inference agents

The newest adversary is not a person at all. Large language models, given public text and a web browser, infer where someone lives and what they do and then search for them, deanonymising at a scale and cost no human profiler could match ([LLM-inference case](cases/llm-inference.md)).

## Black markets

Where data goes to die, repeatedly. Not all data stays in the warm embrace of marketing; once breached, leaked or scraped, much of it ends up on dark-web forums where anonymity is a feature rather than a concern. There it becomes full identity kits of personal details, financials and login credentials, access-as-a-service to compromised accounts, and stolen data laundered back into above-board systems.

## Marketers and advertisers

The inbox is their playground. Distinct from the advertising machinery, these are the people actively planning campaigns and testing messages, armed with behavioural segments built from a person's data. It shows up as hyper-targeted emails that know too much, A/B testing of click habits without the recipient's awareness, and bought lists that were "ethically sourced", with a wink.

## Insurance companies

Risk assessment with a side of intrusion. Insurance used to be about age and postcode; now it is about lifestyle, spending, health data and what a fridge says about its owner. Insurers buy data to predict "risk" and adjust premiums accordingly, profile health and habits from online behaviour, and treat wearables and activity trackers as feedback loops.

## Employers

Smiling in interviews, snooping on socials. From pre-hire vetting to post-resignation surveillance, employers increasingly use data to measure, predict and control: social-media monitoring with or without permission, employee-monitoring software billed as "just for productivity", and datasets bought to screen applicants "objectively".

## Law enforcement

Lawful, but not always proportionate. Data access in the name of safety is a slippery slope, and agencies can and do request logs, metadata and device access, not always with rigorous oversight. The repertoire runs from surveillance and interception under wide legislative mandates, through pressure on platforms to weaken or backdoor encryption, to predictive policing built on opaque and often biased algorithms.

## State-level intelligence agencies

A different species from domestic law enforcement: better resourced, operating under different legal frameworks, and not always subject to the same oversight structures. National signals intelligence agencies can compel cooperation from platforms, conduct bulk data collection under national security justifications, and operate across jurisdictions in ways that local law enforcement cannot.

The capabilities gap between a national intelligence agency and any individual's privacy controls is considerable. Mitigations that work against opportunistic adversaries may be insufficient here, because what actually constrains an agency of this kind is [law and oversight rather than any technique a person can apply](../surveillance/index.rst), and national security is where that law thins out.

## Stalkers and domestic abusers

Location data, device access, account monitoring and social graph analysis are all used by people seeking to track, control or harm individuals they know personally. This adversary has direct access to the target's devices, accounts, and physical environment in ways that remote adversaries do not, which changes the threat profile significantly. Re-identification barely applies: [someone who already knows the answer](../poweron/index.rst) does not need to infer it, and the defences that assume a stranger assume the wrong thing.

## Private investigators

Operating in the gap between law enforcement capability and public accessibility, private investigators routinely use OSINT techniques, data broker purchases, social engineering, and in some cases legally questionable methods to build profiles on individuals. Their clients range from insurers and employers to estranged relatives and abusive partners.

## Politicians

Regulate, confuse and occasionally campaign with the electorate's data. From the GDPR to ad microtargeting, politicians often sit on both sides of the privacy fence, demanding protections while quietly exploiting the system for elections: crafting regulation with loopholes wide enough to drive a tractor through, partnering with platforms for campaign data and targeting, and using fear to justify expanded surveillance powers.

Last reviewed: 2026-07-17.
