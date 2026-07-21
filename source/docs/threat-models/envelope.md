# Reading the envelope: what extraction can afford

A product announcement is close to unforecastable. A datacentre is not. One is decided in a
quarter by people who could have decided otherwise; the other is a multi-year commitment of
capital, land and grid capacity that was visible long before anything was announced.

[Reading the envelope](https://broomstick.tymyrddin.dev/posts/reading-envelope/) makes that trade
deliberately, watching slow constraints instead of fast decisions. The constraints move over
quarters and years, which makes them legible in advance, and the price of the legibility is
precision. Readings of this kind come out directionally right and chronologically early. Anyone
wanting a date is better served elsewhere.

The same gauges can be built for the data economy. They describe what collection can afford to do,
not what any particular firm will try.

## What pays for all of it

Behavioural extraction is funded, still, almost entirely by advertising. That is the master gauge,
and its important property is that it does not expand because a pipeline would like it to.
Advertising has held a fairly stable share of economic activity across decades, through several
technology cycles, which puts a ceiling over everything built to serve it. Collection can get more
precise, cheaper, and more invasive without the pot getting larger.

Most of the industry's strategic behaviour over the past decade reads as an attempt to get out from
under that ceiling. Retail media networks, subscription tiers, payments, data licensing, and sales
into credit, insurance, employment screening and government all move revenue away from the auction
and toward buyers with separate budgets. The [landscape of commercial
extraction](commercial-data-extraction/landscape.md) describes the resulting
sprawl.

The number worth watching is not headline advertising spend. It is the share of a platform's
revenue arriving from anywhere other than advertising, because that share measures how much of the
system has found a second funder.

## What identifiers are still available

The second master gauge is the supply of stable identifiers, and it behaves much like component
access does for a war economy: a ceiling that lowers slowly and forces substitution downward rather
than a stop.

Cookie deprecation, mobile advertising identifier restrictions and app tracking permissions
degraded collection without ending it, and degradation leaves a signature. Deterministic joins give
way to probabilistic matching. Hashed email spreads as a fragile deterministic substitute that
depends on people using one address. Client-side tags move server-side, where a publisher relays
what a browser would have blocked. Clean rooms appear as a contractual workaround for a technical
loss, letting two parties compute over data neither can hold. Each step costs accuracy, and each is
adopted because the previous rung is gone.

Falling match rates and rising reliance on modelled rather than observed audiences are the readable
symptoms. At ground level this is the same gauge a reader touches when they [reset an advertising
identifier](../runbooks/adids.md) or [turn off Topics](../runbooks/disable-chrome-topics.md): the
individual gesture is small, and it is small in a direction the whole industry is being pushed.

## Whether a second buyer arrives

Model training created something the data economy had not previously had, which is a large buyer of
behavioural and content archives that is not an advertiser. Whether that demand hardens into a
durable revenue line or resolves into a handful of one-off licensing deals is the open question
with the widest downstream effect, since a genuine second buyer would fund collection that
advertising economics could never justify on its own.

This gauge is faster-moving than the others and borrows its slowness from underneath. The demand
appeared quickly; the compute, fabrication capacity and power supporting it are physical
commitments measured in years, and those are forecastable even when the demand is not. Where the
buildout continues past the point the current revenue supports, somebody is betting on the second
buyer being real.

## The cost of keeping everything

Falling storage cost is the standard explanation for why retention beat deletion, and as a gauge it
has gone stale. A cost that only ever falls behaves as a constant, and constants do not predict
anything.

The live version is holding cost weighed against the expected value of holding, and recent movement
has come from the supply side rather than the demand side: constrained memory and drive supply,
grid connection queues, and power as the binding input for anything doing inference at scale. Where
retention starts carrying a real marginal cost again, minimisation acquires an ally it has not had
for twenty years, which would be an odd and welcome way to win an argument.

## What a regulator can actually process

Statutes are the wrong thing to count, and
[second-order effects](second-order-effects.md) already sets out how unevenly the
written rules land. The forward-reading number is capacity:
caseworker headcount, time from complaint to decision, how many large investigations an authority
can run at once, and whether penalties are collected or appealed into irrelevance.

Capacity changes over budget cycles, which makes it slow enough to read and slow enough that a
sudden statute rarely changes it. The private channel belongs on the same gauge and moves faster:
class actions and cyber insurance price risk on a commercial clock, and insurers reshape behaviour
through exclusions rather than judgements.

## Where the ground itself sits

The slowest gauge, and probably the most genuinely predictive. Two mobile operating systems decide
what an application is able to observe. A few cloud providers host most of the processing. A small
number of exchanges clear most of the demand. Very little in this domain happens without passing
through one of them.

Concentration cuts both ways, which is what makes it interesting rather than merely grim. It makes
extraction efficient, and it makes regulation tractable, because a rule aimed at four companies can
be enforced in a way that a rule aimed at forty thousand cannot. It also means a platform policy
change can accomplish in one release what a directive spends six years failing to achieve, and that
the same power is available for the opposite purpose. Where that concentration ends up sitting is
argued at [companies](../strategy/companies.md) and, where states are the actor, [nations and
states](../strategy/nations.md).

## Disposition changes the response, not the price

Constraints set the option set. They do not pick from it, and identical conditions produce opposite
behaviour depending on who is facing them.

Ownership structure, time horizon and exposure to a consumer brand all modify the response. Founder
control through dual-class shares tolerates regulatory risk differently from quarterly earnings
exposure, and private equity ownership ahead of a sale differently again. Facing the same
identifier scarcity, one firm degrades gracefully into contextual advertising while another
escalates into fingerprinting, and the difference is disposition rather than arithmetic. States
enter here too, since a government finding the commercial ecosystem a convenient source of its own
intelligence is not a neutral party to that ecosystem's constraints.

This is also why sanctions-style predictions disappoint in both domains. Pressure applied to
revenue is tolerated far longer than pressure applied to survival, and the two get measured as
though they were the same gauge.

## What the envelope will not say

It gives no dates. It names no specific move, and it cannot rank which firm goes first. Several of
its gauges are measured through figures published by the industry being measured, which is a real
weakness rather than a formality. A single ruling or one platform release can outrun every reading
on the list.

The gauges were selected for slowness, so the method is blind to fast shocks by construction and
will read them as surprises afterwards. That is the cost of the trade, and it is worth paying only
for the narrower question the method actually answers: which of the current arrangements are being
held up by a constraint that is loosening, and which are quietly becoming unaffordable.

That question is what makes [systems effects](../strategy/systems.md) actionable rather than merely
true. The homeostatic trap, a system's resistance to reforms that would cut the function it is
optimised for, explains why the equilibrium holds; the gauges indicate where it is under load. The
backward-facing companion, reading a claim against what was already true, is [residue](residue.md).

Last reviewed: 2026-07-19.
