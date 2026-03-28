# Impacts

Even the most carefully tended greenhouse can be ruined if someone tampers with the soil, overfeeds
the aphids, or simply barges in and starts tagging your petunias. The impacts of privacy breaches
and data misuse are not just theoretical. They are personal, structural, and often quietly devastating.

Here is what can go wrong when the data compost heap is turned over too eagerly. Sections marked ↑
describe risks that are growing; those marked ↓ describe things being eroded.

## ↑ Data

Data is the new fertiliser, and everyone wants more of it. Companies scrape, hoard, and analyse as
much as they can, convinced that quantity equals quality. But adding more data to a bad model is like
pouring Miracle-Gro on knotweed: the problem just grows faster.

Yes, recommending the right shoe size is handy. But context is everything.
Imagine you are permanently in a wheelchair and, out of curiosity or kindness, browse a product you
would never use yourself. That brief detour now blooms into an advertising campaign across your
digital life, pushing products you cannot use.
Or you are a teenage girl, and your browsing of a baby product site triggers unsolicited catalogues
sent to your home. A little click, a lot of consequence.

Big data can feel less like insight and more like invasive species, clogging the ecosystem. The root
of the issue? Many assume that more data equals better data. It does not.

* Sometimes less is more: clean your data, prune the outliers, sample wisely.
* Add different features, not just more of the same weeds.
* Models with high bias do not benefit from more training data. They need complexity.
* Models with high variance are overgrown. Cut features. Add control.
* Complex models can become so entangled they cannot scale: the digital equivalent of a vine
  strangling its own trellis.

In short: if your analytics garden is full of noise, do not keep turning up the volume. Learn to
listen better.

## ↑ Bias and discrimination

AI was meant to be the rational gardener: pruning with precision, impartial and tireless. Instead,
we built topiary nightmares that reflect our own worst habits.

Bias is not just a side effect. It is often built in. The systems are opaque, the data is messy,
and the consequences are real:

* Tay, Microsoft's chatbot, famously turned racist in less than 24 hours after being exposed to
  the internet. Like a greenhouse fungus, it thrived on what it was fed.
* HR algorithms that downgrade CVs from women, minorities, or older applicants because their
  profiles do not fit the mould, as if hiring decisions were a matter of preferred soil pH.
* Loan models that exclude students from poor areas because their postcodes are "risky". No loan,
  no education, no way out: a vicious composting cycle.
* DNA test companies handing anonymised health data to insurers. The averages may stay the same,
  but the premiums certainly do not, especially for subgroups already under strain.

Models reward the lucky, punish the rest, and rarely apologise. Worse, the solution often presented
is to "add a human in the loop." But humans are where the biases came from. They just taught the
machine to be more efficient about it.

Avoiding bias is not rocket science:

* We have the techniques.
* We have the tests.

What we apparently lack is the incentive. Bias, like poor security in the past, is not profitable
to fix. At least not yet.

## ↓ Competition

Data has become the prized orchid of the tech world: valuable, delicate, and aggressively protected.

* Microsoft bought LinkedIn for $26.2 billion.
* IBM acquired Truven Health for $2 billion, buying records for over 200 million patients.
* Google scooped up résumés and job data from over 200 million people to fine-tune its
  employment tools.

This is not just capitalism in bloom. It is an arms race. The more data you have, the more you can
learn, the more you dominate. It is the network effect: the biggest platforms pull in more users,
more advertisers, and more data, until moving elsewhere feels impossible.

The result is a landscape where privacy is a luxury rather than a standard, because you are not
really the customer. You are the crop.

## ↑ Surveillance and tracking

Once upon a time, surveillance was about trench coats and binoculars. Now it is about cookies,
clickstreams, and whether your smart toaster knows you skipped breakfast.

We are all being tracked. Always. Some examples are explicit: you click "Accept Cookies" and move
on. Others are implicit: no action needed, just existing in digital space is enough.

* Implicit data includes your order history, page views, and search terms, all logged and
  repurposed.
* First-party tracking is done by the site you are on. Amazon uses it to suggest products based
  on what you and others like you have browsed.
* Third-party tracking follows you across sites, devices, and locations. That Like button reports
  home even if you do not click it.

With mobile phones, it gets worse:

* Your location is constantly tracked. For directions, certainly, but also for marketing.
* Smart devices watch your habits: what you watch, when you sleep, how often you boil your kettle.
* Somatic surveillance tracks your body: heart rates, sleep cycles, even fertility. Insurance
  companies are taking notes, rest assured.

Surveillance exists because it is cheap and easy, and because fear pays:

* Governments surveil to control.
* Corporations surveil to profit.
* Both say it is for your safety.

When every aspect of your life can be monitored, logged, and monetised, privacy is not just under
threat. It is being composted.

## ↑ AI and model exposure

As AI assistants and large language models become embedded in daily work, a new exposure surface
has opened. Data submitted to external AI services may be logged, used for further model training,
or stored in jurisdictions with different legal protections. Queries that seem innocuous in isolation
can be identifying when combined with usage metadata or cross-referenced with other data sources.

LLMs trained on scraped web data have been shown to memorise fragments of their training corpora,
including personally identifiable information, and can sometimes be induced to reproduce them.
The model itself becomes a data leak, independent of what security controls surround the original
training data.

See also: [AI profiling techniques](../../code/ai-profiling.md).

## ↑ Regulation

Laws exist. Sort of. But the weeds grow faster than the hedges.

The GDPR tries to impose order in the private sector, but it does not prevent EU member states
from running their own programmes. Law enforcement and intelligence agencies operate under
different frameworks entirely, and the garden gate does not close neatly across borders.

Jurisdictional arbitrage is a related problem: companies and adversaries route data processing
through whichever legal framework offers the least resistance, making regulation that applies
clearly in one country effectively optional in another. A right that exists on paper in Germany
may be unenforceable against a processor based elsewhere.

Social media adds further complications:

* It blurs the line between public and private. Is your tweet public? What about the location
  metadata attached to it?
* There is a long history of disproportionate surveillance on marginalised communities, including
  profiling, infiltration, and covert monitoring.
* Social media content is sometimes used as evidence, but nuance is lost. Your snarky comment
  may not survive data mining intact.

Legal scholars have started distinguishing OSINT (open source intelligence) from SOCMINT (social
media intelligence), the latter being murkier and more prone to misuse.

EU regulators write the rules that force everyone else to behave, or at least to pretend. Their
tools include GDPR, ePrivacy, the right to be forgotten, and increasingly large fines for data
abuse when enforcement finally lands. The ongoing tug-of-war between EU regulators and major
platforms over data sovereignty is one of the few places where the balance of power is even
partially contested. The EU's ePrivacy regulation promises tighter control of cookies and
trackers, possibly more stringent than GDPR. Whether it turns out to be a new hedge or just
another decorative trellis remains to be seen.

As companies entrench their position with proprietary datasets, competition policy is starting
to notice. Who controls the data controls the future, and the regulators
are finally waking up.

## ↑ Datafication of the self

Personal worth becomes a metric: engagement rate, credit score, productivity level, likes,
followers, sleep cycles. You are no longer a person. You are a performance indicator.

This creates stress, alienation, and a strange new kind of inequality: algorithmic precarity.
If your data profile does not match what the system thinks is "successful," your options
quietly shrink.

It is not just surveillance. It is data feudalism.

## ↑ Loss of context and consent

Data, once collected, is decontextualised and repurposed in ways the original person never agreed to.

You gave your postcode for delivery. Now it is used to decide your insurance premium.
You liked a tweet making a joke about depression. Now an algorithm thinks you are vulnerable.
You uploaded a face to an app. Now it is training someone else's facial recognition system.

Consent is not just "I clicked agree." Real consent is informed, specific, and revocable. The
current system pretends at consent but delivers functional coercion.

## ↑ Global inequity

Most regulations like GDPR are regional. Meanwhile, many developing countries lack the
infrastructure, legal frameworks, or economic leverage to push back against major
data-hungry platforms.

The result is a digital colonialism dynamic. Rich countries export surveillance tools, extract
data, and impose their standards. Poorer regions become both test beds and resource mines, with
little say in what happens to either.

## ↓ Accountability black holes

When something goes wrong (a wrongful arrest, a job rejection, a loan denial due to automated
profiling), it is hard to trace:

* Was it the model?
* Was it the data?
* Was it the person who trained it?
* Or the person who used the output?

These systems create accountability gaps where no one is clearly at fault, and the harmed person
has no clear path to recourse.
