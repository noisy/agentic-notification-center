# INT-005 - Anything that happens to me can reach the agent that cares about it

- actor: owner
- source: owner, 2026-08-24, in noisy-coding issue #39: the daemon "already is
  ~2/3 of a notification center... what it lacks is an INPUT for events that
  are not voice." Named sources: pipelines, chat, mentions, mail, monitoring,
  tickets.
- intent: **I want a pipeline finishing, a message arriving, or a person
  speaking to reach my agents by the same road, so that adding a new kind of
  event does not mean building a new mechanism.**

Rationale: the machinery for carrying a human voice to a working agent -
queueing it, delivering it into a live turn, waking an idle one, ordering it
by importance - is the same machinery every other source needs. Building it
once per source produces five half-implementations that fail differently, and
the fifth source never gets built at all because it is not worth the effort.
Voice is not special; it was merely first.

## Success conditions

1. A new source of events can be added without changing how existing sources
   are delivered, ordered or spoken.
2. Human speech is one source among several, with no privileges the others
   cannot have.
3. Repeated notice of the same underlying fact does not reach an agent
   repeatedly. A flapping pipeline is one item, not fifty.
4. A source that becomes noisy can be silenced by a person, immediately, at the
   source rather than by muting everything.
5. An event that nobody consumed is still visible to a person afterwards.
6. Losing an event is a reportable fault, not an accepted cost of being busy.

## Not prescribed

The wire format; whether sources push or are polled; how deduplication decides
that two events are the same underlying fact; what the ordering rules are;
which sources exist first.
