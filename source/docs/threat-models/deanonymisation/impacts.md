# Impacts

A greenhouse can be ruined without breaking a pane: tamper with the soil, overfeed the aphids,
or just barge in and start tagging the petunias. In this one, every harm runs through a single
event: a record that was meant to be anonymous acquires a name. Before that moment the exposure
is only potential; after it, it is personal, and everything downstream, being profiled, priced,
judged, or approached, needs the naming to have happened first. Neither harm below is receding;
the naming only gets cheaper and surer with each year.

## ↑ Being named

Anonymity is a hedge before it is a technicality. While a record cannot be tied to a
person the harm in it stays latent; the moment it can, the harm becomes theirs to carry.
Re-identification is that moment, and the [three kinds of disclosure](objectives.md) mark what
gets carried: a name fixed to a record, a sensitive fact fixed to a name, or a web of
relationships laid open.

What makes it heavy is that some of it does not wash off. A cleared cookie is replaced; a face,
a gait, or a genome, once linked to an identity, tends to stay linked, and the link can reach
people who never consented and relatives who never tested. It is heaviest for those whose safety
depended on not being found: a whistleblower, an activist under a nervous government, someone
who left an abuser and needed to stay lost.

## ↑ AI and model exposure

As AI assistants and large language models become embedded in daily work, a new exposure surface has opened. Data
submitted to external AI services may be logged, used for further model training, or stored in jurisdictions with
different legal protections. Queries that seem innocuous in isolation can be identifying when combined with usage
metadata or cross-referenced with other data sources.

LLMs trained on scraped web data have been shown to memorise fragments of their training corpora, including personally
identifiable information, and can sometimes be induced to reproduce them. The model itself becomes a data leak,
independent of what security controls surround the original training data. And the same models turned outward infer
identity from ordinary writing ([techniques](techniques.md), [LLM-inference case](cases/llm-inference.md)).

See also: [AI profiling techniques](../../code/ai-profiling.md).

## Past the naming

The effects that reach beyond any single re-identification, bias baked into automated
decisions, the slow reduction of a life to metrics, the concentration of data in a few hands,
are not particular to this model. They belong to all of them at once, and are gathered in
[second-order effects](../second-order-effects.md).

Last reviewed: 2026-07-17.
