# Techniques

Every greenhouse has pests, and in this one the attackers come equipped. These are the methods adversaries
actually use to move from "I wonder who that is" to "I know exactly who that is": the vectors they follow,
the tools they wield, and the structural tricks they exploit when technical ones fall short.

## Re-identification

The goal made method. Re-identification is the process of taking supposedly anonymous data and working
backwards to the individual it describes, using auxiliary information, cross-referencing, or sheer
persistence.

This includes trail re-identification: following the digital footprints that accumulate across browser
sessions, location check-ins, genetic data platforms, and even Tor traffic timing patterns. It is like
putting flour on the greenhouse floor and then acting surprised when someone's footprints lead all the
way back to the watering can. The trail does not have to be obvious to be useful.

Using auxiliary data from a second source, an adversary can match anonymous records against known profiles.
If your anonymised dataset includes someone who bought a specific combination of products on a specific
day, and a public loyalty card breach contains the same combination, the "anonymous" record is no longer
anonymous.

## Classification and inference

This is the nosey neighbour approach: staring through the hedge until the pattern is familiar enough
to make a confident guess.

Classification analysis uses known attributes to predict hidden ones. Link-based classifiers infer
properties from your social graph: if everyone in your cluster holds a particular political view, the
model assumes you do too. Group-based classifiers rummage through browsing history and purchase behaviour
to assign you to segments you never signed up for.

Inference attacks take a small amount of data and extrapolate. An adversary does not need to know your
name to decide that someone who browses specific health forums, lives in a small postcode, and works
unusual hours is almost certainly one of three people. From there, it is a short walk to one.

## Feature and similarity matching

The "you look familiar" technique. Feature matching compares an anonymous data profile against a known
one to find a plausible match, using cluster analysis, statistical similarity, and behavioural fingerprints.

It is not always precise and does not need to be. Amazon's "people who bought A also bought B" logic,
turned adversarial, becomes "people who tweeted this also live near here and probably own a dog." Enough
overlapping features and the identification becomes probabilistic but convincing.

## Graph matching

For adversaries with whiteboards and string. Graph matching ignores names entirely and focuses on
structure: who is connected to whom, how often, and when.

Even fully scrubbed social graphs retain a distinctive shape. If your network of contacts is unusual
enough, the structure alone identifies you as a node, regardless of what the node is labelled. Adversaries
can match graphs from different datasets against each other, seed a target network with fake accounts to
track connectivity patterns, or stitch together multiple breach datasets over time to build a composite
structural map. Once the shape is known, the name is a formality.

## Sparsity-based attacks

Some data is dense. Other data is sparse: a few data points, infrequent transactions, unusual locations.
Counterintuitively, sparse data is often more dangerous.

Sparsity-based techniques exploit the fact that rare behaviours are inherently identifying. If you are the
only person in a dataset who attended a particular event, lives in a small village, and has an unusual
medical history, those three facts alone may be sufficient. A 2013 study by de Montjoye et al. found that
just four approximate location points are enough to uniquely identify 95% of individuals in a mobile
dataset. Anonymisation that works for common profiles tends to fall apart at the edges.

## Data linkage

If they can link your anonymous data from multiple sources, they can build a picture that none of those
sources could provide alone. Linkage attacks start with fragments: a postcode from one breach, an age
bracket from another, a purchase pattern from a third. Stitched together, the fragments form a portrait.

See also: [linkage techniques in code](../../code/linkage.md).

## Membership inference

A subtler attack, and a growing concern in machine learning. Membership inference asks not "who is this
person" but "was this person's data used to train this model?"

Given a trained model and a data record, an adversary can probe the model's confidence on that record.
Models tend to behave differently on their training data than on data they have never seen: they are more
certain, more accurate, less surprised. That difference in behaviour leaks information. In contexts where
model training data is sensitive (medical records, financial histories, private communications), confirming
membership is itself a privacy breach, before any re-identification has occurred.

## Model inversion

Where membership inference asks whether someone was in the training set, model inversion attempts to
reconstruct what was in it.

By querying a model repeatedly with crafted inputs, an adversary can reverse-engineer approximate
representations of training data. Early demonstrations recovered recognisable facial images from facial
recognition models. More recent attacks can extract text fragments, structural patterns, or statistical
signatures from language and tabular models. The model itself becomes the data leak, regardless of how
carefully the original training set was protected.

## LLM and AI exposure

Large language models and AI assistants introduce a distinct exposure surface. When personal or sensitive
data is submitted as part of a prompt, it may be logged, used in further training, or processed by
infrastructure outside the user's jurisdiction. Queries that seem innocuous in isolation can be
individually identifying when combined with usage metadata.

Beyond prompt leakage, LLMs trained on scraped web data may have memorised personally identifiable
information from their training corpus and can be induced to reproduce it. Adversaries can probe models
with targeted queries to extract fragments of memorised content, including names, contact details, and
private documents that happened to be indexed.

See also: [AI profiling techniques](../../code/ai-profiling.md).

## Data poisoning

Classic garden sabotage: mix something toxic into the compost and watch the crop go wrong.

Data poisoning involves introducing false or misleading records into a dataset to corrupt the models
trained on it, skew the results it produces, or create backdoors that can be exploited later. The
poisoned data looks legitimate at ingestion. By the time the effects show up in production outputs, the
source is hard to trace and the damage is done.

## Sybil attacks

The attacker does not try to understand you. They try to become you, repeatedly.

Sybil attacks introduce large numbers of fake identities into a network or system, each behaving slightly
differently to probe for information, manipulate social graph analysis, or dilute the reliability of
anonymisation schemes that depend on group size. A k-anonymity scheme that requires at least ten people
sharing your attributes is considerably less reassuring when five of those people are sock puppets.

## Collusion attacks

Sometimes pests collaborate. Collusion attacks occur when multiple adversaries pool information they
hold separately, combining it to break anonymisation that would resist any single party's data alone.

Two organisations each holding partial records that individually satisfy privacy requirements may together
hold enough to uniquely identify individuals. This can be deliberate coordination or an unintended
consequence of data sharing arrangements that seemed innocuous in isolation.

## Legal and regulatory attacks

Not all attacks arrive at night. Some arrive on headed notepaper.

Regulatory or legal compulsion can force disclosure of data that was otherwise protected: court orders,
national security requests, and broadly worded "legitimate interest" provisions can all override
technical protections. Jurisdictional arbitrage allows adversaries to route requests through whichever
legal framework offers the least resistance. The data may be safe from hackers and perfectly exposed to
the law.

## Data exfiltration

The classic quiet exit. Exfiltration is the extraction of data from a secure environment, usually
incrementally and under the radar: a few records at a time, disguised as normal traffic, or piggybacking
on legitimate integrations. By the time the loss is detected, the data has long since changed hands.
