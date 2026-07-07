Naming the anonymous: a deanonymisation threat model
=====================================================

In a greenhouse, everything is visible, even the things pushed to the back of the compost bin.
Not every door needs locking, nor every shadow fearing. What counts is who might be
poking around the potting shed, what they are after, and how they get it.

It takes an attacker's-eye view of the terrain, from the assets ripe for the picking to the sour
soil left behind.

Where the :doc:`surveillance model <../surveillance/index>` is about who watches and how the
collection is built, this one is the layer above it: the techniques that turn collected, published,
or "anonymous" data back into a specific person. Surveillance gathers; deanonymisation names. It is
the same move the :doc:`infrastructure-aggregation model <../infrastructure-aggregation/index>` makes
on buildings and cables, the combination is the finding, applied to people instead. And when the
adversary is not a state or a broker but someone who already knows the target, the
:doc:`poweron model <../poweron/index>` is the intimate-range version of the same techniques.

.. toctree::
   :glob:
   :maxdepth: 1
   :includehidden:
   :caption: When the data is the fertiliser, it is worth knowing who is doing the planting.

   assets.md
   adversaries.md
   objectives.md
   techniques.md
   assistive.md
   cases/index
   mitigations.md
   impacts.md
   consent.md
