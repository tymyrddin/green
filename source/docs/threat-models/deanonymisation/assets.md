# Assets

Welcome to the greenhouse's hidden treasures: the juicy, leafy data crops adversaries are after.
Whether tucked safely behind fences or left out for the taking, every dataset tells a story. Here
is what is growing, and what makes each variety so appealing.

## Data releases

Think of data as different levels of greenhouse access. Sometimes it is just the head gardener
poking about with good intentions. Other times, the gates are flung open and tourists can trample
through at will. Here are the flavours:

### Internal secondary research

This is the "we are just looking around the shed" kind. Internal teams reuse data they already had
permission for, usually with some vague notion of anonymisation. The risk of external intruders is
low, in theory, since access is tightly controlled. But let us not pretend an overconfident intern
could not leave the door ajar.

### External secondary research

Here, outsiders are allowed into the garden, but only after signing a blood pact (or a data-sharing
agreement). With anonymisation, contracts, and a few watchdogs, it feels secure. That is, until
someone gets clever with auxiliary information and finds a way to pick the lock. Trust, but verify,
and then lock the compost bin.

### Public release

The wild meadow: data tossed out into the open, ripe for the picking. Anyone with a basket and bad
intentions can gather what they like. It is impossible to know who is harvesting or what tools they
have brought. Here, assumptions about adversary motivation and technical skill do not just backfire.
They explode like overripe fruit.

## Auxiliary information

You might think your data is safe, anonymised and stripped of names. But adversaries are tenacious
compost sniffers, and they will dig through the mulch to find what they need.

* They collect crumbs: bits of information from petitions, forums, even a colleague's old review of
  a garden centre.
* They buy old maps: open datasets, neighbourhood statistics, and that quaint survey from 2009.
* They inherit leftovers: mergers, acquisitions, and shadowy black market data swaps.
* And sometimes they find hints inside the target dataset itself, like a cryptic note left in a
  flowerpot.

In short: they will mix and match with whatever is lying around to figure out what is really growing
in your greenhouse.

## Target dataset

The main crop: the big, labelled "anonymised" but still suspiciously personal collection of records.
The names and phone numbers are gone, replaced with techniques like k-anonymity. But with enough
auxiliary information and determination, the roots are traceable. See [mitigations](mitigations.md)
for what those techniques can and cannot do.

## Biometric data

Faces, voices, fingerprints, gait patterns, and retina scans. Biometric data is uniquely dangerous
because it cannot be changed. A breached password can be reset. A leaked face cannot be replaced.

Facial recognition databases built from scraped social media images, voice prints extracted from
customer service calls, and gait signatures lifted from CCTV footage all create permanent linking
keys that persist across any number of future datasets. See also: [metadata](../../code/metadata.md)
and [browser fingerprinting](../../code/browser.md).

## Location and mobility data

GPS trails, mobile cell tower logs, transport card swipes, and geofenced advertising data. Location
data is among the most re-identifying categories that exists. A 2013 study by de Montjoye et al.
demonstrated that just four approximate location points are sufficient to uniquely identify 95% of
individuals in a mobile dataset.

Continuous location data reveals home address, workplace, religious attendance, medical appointments,
political activity, and intimate relationships, all without a single explicit label.

## Behavioural and temporal patterns

The rhythm of behaviour over time: when you wake up, how long you spend on particular pages, the
order in which you complete tasks, your response latency to notifications. Temporal patterns are
highly distinctive and extremely difficult to anonymise, because the structure of someone's day is
often more identifying than any single data point within it.

Behavioural fingerprints extracted from mouse movement, keystroke dynamics, and scroll behaviour
can re-identify individuals across sessions even after all explicit identifiers have been removed.

## Graph and network data

Your social graph: who you are connected to, how often you communicate, the structure of your
relationships. Graph data is particularly resistant to anonymisation because the re-identifying
information is structural rather than attribute-based. Removing names leaves the shape of the
network intact, and that shape is often sufficient.

This includes contact lists, follower networks, communication metadata, and co-authorship or
co-participation graphs.

## Device fingerprints

Browser configuration, screen resolution, installed fonts, GPU rendering characteristics, time
zone, language settings, and hardware identifiers combine to form a fingerprint that is often
unique to a single device and therefore a single person. These fingerprints persist across
incognito sessions, VPNs, and cleared cookies.

See also: [browser fingerprinting](../../code/browser.md).

## Synthetic data

Artificially generated records designed to mimic a real dataset without containing any real
individuals. Increasingly used in healthcare and finance as a privacy-preserving alternative to
sharing raw data.

Synthetic data deserves its own entry here because it is an asset that carries concealed risk.
It is not automatically safe: generative models trained on small or unusual populations may
reproduce identifying patterns; membership inference attacks can sometimes establish whether a
particular individual's data contributed to the training process. "It is synthetic" is not a
guarantee of safety. It is a starting point for a more careful conversation.
