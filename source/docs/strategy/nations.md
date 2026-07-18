# Nations and states

![Civil](/_static/images/nations-and-states.png)

The EU holds the strongest data-protection framework in the world and, at the same time, contains member
states that run bulk collection programmes, buy from commercial data brokers to clear thresholds they could
not clear directly, and sit in intelligence-sharing alliances that route around whatever their own law
forbids. These are not contradictions. They are the system working as designed. The state is the one
adversary a person cannot opt out of, and its most capable arm, the intelligence services, works precisely
where the protections stop.

Generalisation is especially coarse here: member states vary widely in their legal cultures, their judicial
oversight of intelligence activity, and their appetite for digital sovereignty. The shape of the problem is
common to them; the severity is not.

## The hole where the services live

The national-security exemption in the GDPR is a deliberate design
decision, the one the [surveillance model's legal landscape](../threat-models/surveillance/landscape/the-gdpr-hole.md)
turns on: the EU excluded national-security activity from the regulation's scope, deferring to member-state
sovereignty in the single area where harmonisation was politically impossible. The result is a regime whose
centre is cut out exactly where the most capable actors operate. A person's data is guarded against
commercial misuse by one set of rules and against state surveillance by a patchwork of national law, treaty,
and whatever quality of judicial oversight a given member state happens to run. A strategy that assumes the
framework protects against the services has misread the map.

## The state as aggregator

Interception is the old picture. The newer one is procurement and assembly. Agencies buy location and
behavioural data from the broker market because a purchase does not trip the safeguards a warrant would, and
the [Databroker Files](../threat-models/surveillance/cases/databroker-files.md) showed that this reaches even
EU and NATO officials.

Buying is only half of it. The [administrative attack surface](https://purple.tymyrddin.dev/docs/admin-surface/)
is the other half: routine, individually harmless public records, tenders, planning applications, network
registries, staff directories, combine into a picture no single disclosure intended. At state scale that
logic cuts both ways. It is how an intelligence service assembles a target from open sources, and it is how a
foreign one maps a nation's critical infrastructure without touching a single protected system. The
combination is the finding, and no data-protection right reaches a finding that was never held in any one
record. Sovereignty, at this point, is less about where a server sits than about who is patient enough to
read what a state routinely publishes about itself.

## Routing around the limits

Where domestic law bars a service from collecting on its own citizens, an ally under no such constraint can
collect and hand the result back. The intelligence-sharing groupings the surveillance model describes under
[built-in collection](../threat-models/surveillance/landscape/built-in-collection.md) turn a legal limit into
an administrative inconvenience. A strategy pitched at national law alone tends to miss the transnational
shape of the thing it means to govern.

## The ratchet

Surveillance powers expand after events and rarely contract afterwards. A crisis produces pressure to act,
and "act" is read as more collection and more access far more readily than as more oversight or less
exposure. Expansion can be presented as decisive; oversight reform is slow, technical, and yields nothing a
news cycle can show. The cost of bulk collection is diffuse, statistical, and distant from anyone's direct
experience until a specific incident makes it concrete, which is why political action gathers around named
harms and seldom around the standing condition. Civil society organisations, journalists and researchers who
make the diffuse harm concrete and named are doing the work that creates the conditions for reform.
Supporting that capacity is not adjacent to the strategy. It is the strategy.

## Where the leverage is

Honesty first: at the level of the intelligence services, individual action is close to zero, and pretending
otherwise would be a kind of theatre. Leverage sits with regulation and oversight, and it is real but
unevenly used. EU regulatory capacity has changed the behaviour of global platforms because non-compliance
risks a slice of worldwide revenue; the same pressure, applied consistently to the broker market and to
purpose limitation, could shrink the commercial layer the services buy from. Intelligence oversight itself
remains underdeveloped relative to the transnational collection it is meant to govern: oversight between
national mechanisms does not cover what flows through the sharing arrangements, and a European body with
genuine access to cross-border programmes would be a structural improvement.
None of this dismantles security capacity. It builds governance that matches the capacity already there, and
that has historically moved slowly, incompletely, and sometimes backwards.

Individual action is limited rather than absent, and the rights regulation creates are only useful exercised:
[removing a profile from broker sites](../playbooks/brokers.md) and [submitting a GDPR deletion
request](../runbooks/gdpr-deletion.md) shrink the commercial half of the picture. For an organisation on the
receiving end of a state demand, [responding to a legal demand](../runbooks/legal-demand.md) and [handling a
data-subject request](../runbooks/data-subject-request.md) are the procedures worth having ready before they
are needed.

Last reviewed: 2026-07-09.
