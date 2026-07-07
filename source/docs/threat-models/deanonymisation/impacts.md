# Impacts

Even the most carefully tended greenhouse can be ruined if someone tampers with the soil, overfeeds the aphids, or
simply barges in and starts tagging the petunias. The impacts of privacy breaches and data misuse are not just
theoretical. They are personal, structural, and often quietly devastating.

Here is what can go wrong when the data compost heap is turned over too eagerly. Sections marked ↑ describe risks that
are growing; those marked ↓ describe things being eroded.

## ↑ Data

Data is the new fertiliser, and everyone wants more of it. Companies scrape, hoard, and analyse as much as they can,
convinced that quantity equals quality. But adding more data to a bad model is like pouring Miracle-Gro on knotweed: the
problem just grows faster.

Recommending the right shoe size is handy. But context is everything. Someone permanently in a wheelchair browses, out
of curiosity or kindness, a product they would never use themselves. That brief detour now blooms into an advertising
campaign across their digital life, pushing products they cannot use. Or a teenage girl whose browsing of a baby-product
site triggers unsolicited catalogues sent to the family home. A little click, a lot of consequence.

Big data can feel less like insight and more like an invasive species, clogging the ecosystem. The root of the issue is
the assumption that more data equals better data. It does not.

Sometimes less is more: cleaner data, pruned outliers, wiser sampling, different features rather than more of the same
weeds. Models with high bias do not benefit from more training data; they need complexity. Models with high variance
are overgrown and want fewer features and more control. And complex models can become so entangled they cannot scale,
the digital equivalent of a vine strangling its own trellis.

In short: an analytics garden full of noise is not improved by turning up the volume. The skill is in listening better.

## ↑ Bias and discrimination

AI was meant to be the rational gardener: pruning with precision, impartial and tireless. Instead the result is topiary
nightmares that reflect their makers' worst habits.

Bias is not just a side effect. It is often built in. The systems are opaque, the data is messy, and the consequences
are real. Tay, Microsoft's chatbot, famously turned racist in less than 24 hours of exposure to the internet, thriving
like a greenhouse fungus on what it was fed. Tay was a curiosity, though. The serious version does lasting damage: from 2013 the Dutch tax authority ran a risk-classification model over childcare-benefit claims that scored dual nationality and a non-Dutch-sounding name as markers of fraud, and some 26,000 families were [wrongly accused](https://www.amnesty.org/en/latest/news/2021/10/xenophobic-machines-dutch-child-benefit-scandal/), many driven into debt, bankruptcy, or the removal of their children, with the government resigning over it in 2021 and the data-protection authority later fining the tax service for processing nationality data unlawfully. HR algorithms downgrade CVs from women, minorities or older applicants
because their profiles do not fit the mould, as if hiring were a matter of preferred soil pH. Loan models exclude
students from poor areas because their postcodes are "risky": no loan, no education, no way out, a vicious composting
cycle. And some DNA test companies hand anonymised health data to insurers, where the averages may stay the same but
the premiums certainly do not, especially for subgroups already under strain.

Models reward the lucky, punish the rest, and rarely apologise. Worse, the solution often presented is to "add a human
in the loop." But humans are where the biases came from; they just taught the machine to be more efficient about it.

Avoiding bias is not rocket science: the techniques exist, and so do the tests. What is apparently missing is the
incentive. Bias, like poor security in the past, is not profitable to fix. At least not yet.

## ↓ Competition

Data has become the prized orchid of the tech world: valuable, delicate, and aggressively protected.

Microsoft bought LinkedIn for $26.2 billion. IBM acquired Truven Health for $2.6 billion, and with it the records of
over 200 million patients.

Those were the last era's land-grabs, done by acquisition. The current one is quieter and aimed at AI: platforms rewrite their terms to train models on the content people have already posted, and sign content-licensing deals for the archives they hold, so the value is extracted without the data ever changing hands.

This is not just capitalism in bloom. It is an arms race. The more data a platform has, the more it can learn, and the
more it dominates. It is the network effect: the biggest platforms pull in more users, more advertisers, and more data,
until moving elsewhere feels impossible.

The result is a landscape where privacy is a luxury rather than a standard, because the individual is not really the
customer. They are the crop.

## ↑ Surveillance and tracking

Once upon a time, surveillance was about trench coats and binoculars. Now it is about cookies, clickstreams, and whether
a smart toaster knows breakfast was skipped.

Everyone is being tracked, always. Some of it is explicit: a click on "Accept Cookies" and on with the day. Some is
implicit: no action needed, just existing in digital space is enough.

Implicit data includes order history, page views and search terms, all logged and repurposed. First-party tracking is
done by the site itself, the way Amazon suggests products based on what similar people have browsed. Third-party
tracking follows a person across sites, devices and locations: that Like button reports home even when it is never
clicked.

With mobile phones it gets worse. Location is tracked continuously, for directions certainly, but also for marketing.
Smart devices watch habits: what is watched, when someone sleeps, how often the kettle boils. Somatic surveillance
tracks the body itself, heart rate, sleep cycles, even fertility, and insurance companies are taking notes.

Surveillance exists because it is cheap and easy, and because fear pays. Governments surveil to control; corporations
surveil to profit; both say it is for everyone's safety. Where the state is the one watching,
the [surveillance model](../surveillance/index.rst) sets out how that works and what permits it.

When every aspect of a life can be monitored, logged, and monetised, privacy is not just under threat. It is being
composted.

## ↑ AI and model exposure

As AI assistants and large language models become embedded in daily work, a new exposure surface has opened. Data
submitted to external AI services may be logged, used for further model training, or stored in jurisdictions with
different legal protections. Queries that seem innocuous in isolation can be identifying when combined with usage
metadata or cross-referenced with other data sources.

LLMs trained on scraped web data have been shown to memorise fragments of their training corpora, including personally
identifiable information, and can sometimes be induced to reproduce them. The model itself becomes a data leak,
independent of what security controls surround the original training data. And the same models turned outward infer
identity from ordinary writing, as the [techniques](techniques.md) page and
the [LLM-inference case](cases/llm-inference.md) describe.

See also: [AI profiling techniques](../../code/ai-profiling.md).

## ↑ Regulation

Laws exist. Sort of. But the weeds grow faster than the hedges.

The GDPR tries to impose order in the private sector, but it does not prevent EU member states from running their own
programmes. Law enforcement and intelligence agencies operate under different frameworks entirely, and the garden gate
does not close neatly across borders. That national-security gap is the subject of
the [surveillance model's legal landscape](../surveillance/landscape/the-gdpr-hole.md).

Jurisdictional arbitrage is a related problem: companies and adversaries route data processing through whichever legal
framework offers the least resistance, making regulation that applies clearly in one country effectively optional in
another. A right that exists on paper in Germany may be unenforceable against a processor based elsewhere.

Social media adds further complications. It blurs the line between public and private: is a tweet public, and what
about the location metadata attached to it? There is a long history of disproportionate surveillance on marginalised
communities, including profiling, infiltration and covert monitoring. And social media content is sometimes used as
evidence, where nuance is lost; a snarky comment may not survive data mining intact.

Legal scholars have started distinguishing OSINT (open source intelligence) from SOCMINT (social media intelligence),
the latter being murkier and more prone to misuse.

EU regulators write the rules that force everyone else to behave, or at least to pretend. Their tools include the GDPR,
ePrivacy, the right to be forgotten, and increasingly large fines for data abuse when enforcement finally lands. The
ongoing tug-of-war between EU regulators and major platforms over data sovereignty is one of the few places where the
balance of power is even partially contested. The ePrivacy regulation promised tighter control of cookies and trackers,
possibly more stringent than the GDPR; after eight years of deadlock, the Commission withdrew the proposal in 2025. Not
a new hedge after all, just a decorative trellis that never left the catalogue.

The direction of travel turned in late 2025. The Commission's Digital Omnibus, presented as simplification, would narrow the definition of personal data, open a legitimate-interest route to training AI on people's content, and loosen the consent required to read data from a device; the [surveillance model's deregulation turn](../surveillance/landscape/the-deregulation-turn.md) sets it out in full. For a page about protections being eroded, that is the clearest sign yet that the erosion is being written into law rather than merely tolerated.

As companies entrench their position with proprietary datasets, competition policy is starting to notice. Who controls
the data controls the future, and the regulators are finally waking up.

## ↑ Datafication of the self

Personal worth becomes a metric: engagement rate, credit score, productivity level, likes, followers, sleep cycles. A
person is no longer a person. They are a performance indicator.

This creates stress, alienation, and a strange new kind of inequality: algorithmic precarity. If a data profile does not
match what the system thinks is "successful," the person's options quietly shrink.

It is not just surveillance. It is data feudalism.

## ↑ Loss of context and consent

Data, once collected, is decontextualised and repurposed in ways the original person never agreed to.

A postcode given for delivery is now used to set an insurance premium. A liked tweet joking about depression now marks
someone as vulnerable to an algorithm. A face uploaded to an app now trains someone else's facial recognition system.

Consent is not just "I clicked agree." Real consent is informed, specific, and revocable. The current system pretends at
consent but delivers functional coercion, as the [consent](consent.md) page sets out.

## ↑ Global inequity

Regulations like the GDPR are regional. Meanwhile, many developing countries lack the infrastructure, legal frameworks,
or economic leverage to push back against major data-hungry platforms.

The result is a digital colonialism dynamic. Rich countries export surveillance tools, extract data, and impose their
standards. Poorer regions become both test beds and resource mines, with little say in what happens to either.

## ↓ Accountability

When something goes wrong (a wrongful arrest, a job rejection, a loan denial due to automated profiling), it is hard to
trace. Was it the model, the data, the person who trained it, or the person who used the output?

These systems create accountability gaps where no one is clearly at fault, and the harmed person has no clear path to
recourse.
