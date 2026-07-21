# Reading the residue: claims and what is left behind

A breach notification is drafted in a few hours by people whose task is to be defensible rather
than accurate. The traffic that produced the breach accumulated over months and revises itself for
nobody. [The naming and the finding out](https://broomstick.tymyrddin.dev/posts/eye-on-strait/)
reads a run of staged incidents along that split and finds that confirmation almost never comes
from a sceptic reading the story correctly at the time. It comes later, out of material the story
could not reach: an affidavit, an archive, a device nobody expected to be recovered.

Two questions carry most of the method. Where is the meaning being made, and what is the residue
saying. Where the answers diverge, the divergence is the part worth following.

## Where the meaning is being made

The venue is rarely neutral. A breach notification, a transparency report, a privacy policy, a
compliance certification and an attribution write-up are all produced under time pressure, with
counsel in the room, for an audience that includes a regulator and somebody's litigator. Accuracy
is one constraint among several and seldom the binding one.

None of that requires bad faith. A statement written to survive litigation is optimised for
survival, and the optimisation shows up as vagueness exactly where precision would be expensive.
"A limited number of accounts" is doing work that a figure would not do. "Unauthorised third party"
is doing work that a named vector would not do. The interesting property of such phrases is that
they are usually true, which is what makes reading them as reassurance a mistake rather than a
disagreement.

Residue is the other layer: the record left by systems going about their work, made without an eye
on how it would later read.

## What counts as residue here

Certificate transparency logs record what was issued and when. DNS history records what resolved
where. An app bundle lists the software development kits compiled into it, whatever the policy says
about sharing. Traffic captured from a device someone owns shows what the application contacts on
launch. Regulatory filings carry timestamps. Court exhibits carry documents nobody drafted for
publication. Job adverts describe infrastructure that has not been announced, because a team hiring
for a data platform will describe the data platform in order to fill the post.

Here the analogy with the historical cases breaks, and for once it breaks favourably. Gleiwitz
waited six years for an affidavit and Mainila waited half a century for an archive. A good deal of
privacy residue is available this week, to anyone willing to put [a proxy in front of a
phone](../playbooks/pcapdroid.md) or to file [a subject access
request](../runbooks/data-subject-request.md) and read what comes back against what the policy
promised. The delay that makes historical confirmation a matter for the next generation is, in this
domain, sometimes an afternoon.

## The first days of a real incident are a mess

Genuine incident response is underdetermined for weeks. Scope estimates move, the initial access
vector gets revised, victim counts go up rather than down, and the people closest to it decline to
commit to a number because they do not yet have one. That confusion is a signature of the real
thing, and the source essay makes the same observation about events that were not staged: they
spend their first days being confusing.

A statement arriving on day two, complete, bounded, and carrying a reassuring negative, is
therefore a document about drafting rather than a document about forensics. "No evidence of access"
is the phrase doing the most work here. It is true of any organisation that was not logging, and its
truth conditions are satisfied by not having looked. Nothing about it is dishonest. It simply
reports the state of somebody's evidence, which is a different claim from the one most readers take
from it.

The related tell is a disclosure that gives a breach date and omits a detection date. The gap
between the two is the number that would characterise the failure, and its absence is a choice.

## The capability was already there

Of the patterns in the source essay, lead times transfer most cleanly. Wars run on logistics
measured in months, so the preparation predates the pretext and is more legible than the pretext.
Data collection runs on engineering, which leaves the same kind of trail.

The software development kit ships before the consent flow that authorises it. The retention
pipeline predates the notice explaining why retention is necessary. Training infrastructure gets
built, staffed and paid for well before the terms update that permits training on what users
already posted. Contracts, job adverts and capital commitments all date earlier than the
announcement, and each is easier to verify. Where observed traffic has contradicted a stated
policy, as in the [Meta pixel](commercial-data-extraction/cases/meta-pixel.md),
[Avast](commercial-data-extraction/cases/avast.md) and
[Flo](commercial-data-extraction/cases/flo.md) cases, the contradiction was generally visible in
the wire before it was conceded in a statement.

This is the same move [substrate](substrate.md) makes across an era, applied to a single
organisation over a couple of quarters. The stated reason rotates. What was built stays built.

## Refusing to look is a finding

Access behaviour carries information of its own. Incident forensics routed through outside counsel
so the report attracts privilege. Settlement terms that bar a researcher from publishing. Audit
scopes drawn to exclude the system that failed. Bug bounty conditions converting a finding into a
secret. Certification against a standard whose boundary was chosen by the certified party.

None of these establishes wrongdoing, and saying otherwise would overreach badly. Each is a
defensible decision with ordinary commercial logic behind it. What they share is that they are
choices about what can be checked afterwards, and a consistent pattern of such choices is readable
even when every individual instance is innocent. Weighing a supplier's account is where this gets
practical, and Green's [vendor assessment](../playbooks/vendor-assessment.md) guide takes the
reading into practice, with [vendor breach](../runbooks/vendor-breach.md) for once something has
gone wrong.

## Chosen for legibility

The accused-side pattern transfers only partly. In the staged cases, a culprit was picked for
legibility rather than capability: someone the audience would find plausible, regardless of whether
they could have done it.

The privacy equivalent is milder and more common. "A sophisticated state-sponsored actor" explains
a failure in a way that exonerates patch cadence, credential hygiene and the decision not to fund
the security team. Most of the time this is blame allocation rather than fabrication, and treating
it as fabrication gets the register wrong.

Attribution proper needs a firmer caveat, because it is the one area where residue is itself the
forgeable layer. Technical attribution rests on artefacts that are cheap to plant: infrastructure
reuse, compile timestamps, language settings, tooling overlap. Olympic Destroyer was built to be
misattributed and duly was, by competent people reading real evidence. Where the traces are
plantable, capability and lead times carry more weight than the traces.

## Where this method goes wrong

The false-flag frame does not carry over, and over-applying it is exactly where this reading goes
wrong. Almost every gap between an infosec claim and infosec reality is explained by institutional
drift rather than by a scheme. Counsel writes the disclosure, marketing writes the policy,
procurement writes the vendor claim, engineering knows something none of them asked about, and no
one coordinates. The result looks coordinated from outside and is not.

The leakage argument from the source essay is the useful brake, and it cuts in the sceptical
reader's favour. Operations need hands that remember, so a story requiring several thousand
engineers to hold a secret for a decade is weak. A story requiring only that nobody was looking is
strong, and the residue usually supports the second. When a claim can be explained by negligence or
by conspiracy, negligence has the better prior and the worse press.

Two further limits remain. Absence of residue is not evidence of concealment,
since a great many organisations are not instrumented well enough to leave any. And much of the
richest material reaches only regulators and litigants under discovery, which makes an individual
reader's version of this method a narrower instrument than the full one.

What it produces, at best, is a reason to ask a sharper question. Reading backwards from a claim to
what was already true is one half of a pair; reading forwards from present conditions to what stays
affordable is the other, and that is
[what extraction can afford](envelope.md).

Last reviewed: 2026-07-19.
