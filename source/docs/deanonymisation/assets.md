# Assets

Welcome to the greenhouse’s hidden treasures — the juicy, leafy data crops adversaries are after. Whether tucked 
safely behind fences or left out for the taking, every plant (read: dataset) tells a story. Here’s what’s growing:

## Data releases

Think of data as different levels of greenhouse tours. Sometimes it’s just the head gardener poking about with 
good intentions. Other times, the gates are flung open and tourists can trample through at will. 
Here are the flavours:

### Internal secondary research

This is the "we’re just looking around the shed" kind. Internal teams reuse data they already had permission for, 
usually with some vague notion of anonymisation. The risk of sneaky intruders is low — in theory — since access is 
tightly controlled. But let’s not pretend an overconfident intern couldn’t leave the door ajar.

### External secondary research

Here, outsiders are allowed into the garden, but only after signing a blood pact (or a data-sharing agreement). 
With anonymisation, contracts, and a few watchdogs, it feels secure. That is, until someone gets clever with 
auxiliary information and finds a way to pick the lock. Trust, but verify — and then lock the compost bin.

### Public release

Ah, the wild meadow — data tossed out into the open, ripe for the picking. Anyone with a basket and bad intentions 
can gather what they like. It’s impossible to know who’s harvesting or what tools they’ve brought. Here, assumptions 
about motivation and technical skill don’t just backfire — they explode like overripe fruit. And yet, we’re told 
it’s all worth it for “data utility.”

## Auxiliary information

You might think your data is safe, anonymised and stripped of names. But adversaries are tenacious compost sniffers, and they'll dig through the mulch to find what they need.

* They collect crumbs — bits of info from petitions, forums, even your colleague’s old Facebook review of a garden centre.
* They buy up old maps — open datasets, neighbourhood stats, and that quaint survey from 2009.
* They inherit leftovers — mergers, acquisitions, and shady black market data swaps.
* And sometimes they find hints inside the target dataset itself, like a cryptic note left in a flowerpot.

In short, they’ll mix and match with whatever’s lying about to figure out what’s really growing in your greenhouse.

## Target dataset

This is the main crop: the big, green bush labelled “anonymised” but still suspiciously personal.

Sure, the names and phone numbers are gone, replaced with jargon like k-anonymity and l-diversity. There's even a 
new kid on the compost heap — differential privacy. But the reality? The greenhouse might look tidy, but with enough 
auxiliary info and determination, it’s not that hard to trace the roots.

### k-Anonymity & friends

Sounds clever, right? Basically, it tries to make each plant look like several others so you can’t tell which is which. 
Trouble is, if someone already knows where the roses are planted, this disguise won’t stop them.

### Differential privacy

A smarter idea, in theory. It adds a bit of noise — think scarecrows in the wrong places — so no one can be sure 
which individual sprouted which trait. But the results can end up being either too vague to use or too leaky to 
be safe. Still, it’s the poster child for privacy these days — just don’t stare too hard at the cracks.