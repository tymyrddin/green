# The model that reads between the lines

The newest re-identification engine is the large language model, and it needs no leaked dataset to work. It reads ordinary writing and infers the author.

## What the research shows

In 2023 researchers at ETH Zurich (Robin Staab, Mark Vero, Mislav Balunović and Martin Vechev) showed that current large language models can infer personal attributes, location, income, sex, age and more, from ordinary online text, at [up to 85% accuracy for the top guess and 95% within the top three](https://arxiv.org/abs/2310.07298), working from Reddit comments that carried no explicit personal detail. They did it at a fraction of the cost and time a human profiler would need. The paper, "Beyond Memorization: Violating Privacy via Inference with Large Language Models" (ICLR 2024), also tested the obvious defences and found them wanting: text-anonymisation tools and model alignment did not reliably stop the inference.

Later work extended it from inference to identification. Agentic systems, models given a web browser, can take a handful of anonymous comments, infer where a person lives and what they do, search the open web, and propose a name, recovering identities by cross-referencing details against public pages.

## Why it counts

This closes a gap the older techniques left open. [Stylometry](../techniques.md), authorship attribution by writing style, used to need a candidate shortlist and specialist tooling; a language model does the same work at scale, from a standing start, with no shortlist at all. It also defeats the assumption behind most text-based privacy advice, that removing names and obvious identifiers is enough. It is not, once the reader is a model that reasons from the incidental. The capability sits directly alongside the [surveillance model](../../surveillance/index.rst): the text people publish becomes another route from data to identity, one that needs no interception at all.
