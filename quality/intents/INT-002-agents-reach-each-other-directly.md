# INT-002 - My agents reach each other directly, without me carrying the message

- actor: owner / any person running more than one agent
- source: owner, 2026-09-05: "I'm trying to figure out how you and Codex could
  communicate without me as a mid proxy." At the time, every exchange between
  two agents was being spoken to him and retyped by him.
- intent: **I want two of my agents to hold a working conversation with each
  other while I watch, rather than through me.**

Rationale: a person relaying messages between two agents is slower than either
of them, loses detail on every hop, and turns collaboration into dictation.
It also scales badly in the most literal way: three agents make three channels,
four make six, and the person is on all of them. The value of several agents is
that they can disagree with each other and resolve it; that cannot happen if
every exchange has to pass through a human's attention and voice.

## Success conditions

1. An agent can address another agent it did not start, and be addressed by
   one, without a person copying anything.
2. A message reaches a busy agent without interrupting what it is doing, and
   reaches an idle one without a person nudging it.
3. An agent that cannot be woken by the system can still take part - it
   receives what was sent while it was away, in order, when it next surfaces.
4. Participation does not require both agents to be the same product, the same
   vendor, or to have the same capabilities.
5. The person can see the whole exchange, during and after, without having
   been part of it.
6. An exchange between agents leaves a record that outlives the agents' own
   memory of it.

## Not prescribed

The transport; whether messages are point-to-point, subscribed by topic, or
both; how an agent is named or discovered; whether delivery is push or pull;
what a harness must implement to participate, beyond the requirement in (3)
that a minimal one still can.
