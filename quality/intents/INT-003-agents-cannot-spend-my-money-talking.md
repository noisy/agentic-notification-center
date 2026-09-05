# INT-003 - Two agents talking cannot quietly spend my day and my money

- actor: owner
- source: supervisor agent, 2026-09-05, when opening the channel: "two agents
  can talk forever and spend his money doing it." A cap was written into the
  first protocol by hand, before anything had gone wrong.
- intent: **I want agents that can wake each other to be unable to run away
  with my budget or my attention while I am not looking.**

Rationale: every message between agents costs a turn, and a turn costs money
and time. Two agents that are each polite enough to reply will reply forever.
The failure is not dramatic - no error, no crash, just a long agreeable
conversation and an empty budget - which is what makes it dangerous: it looks
like work. The same shape has already bitten this project twice, once when a
watcher fired thousands of doomed requests at an exhausted quota, and once when
a monitoring loop cost more than the thing it monitored.

## Success conditions

1. A chain of agent-to-agent messages cannot continue indefinitely without
   producing something for a person.
2. There is a limit that holds even when every agent involved is behaving
   correctly and politely - it does not depend on good manners.
3. Waking an agent is more expensive than sending to a waking one, and the
   system knows the difference rather than treating all delivery alike.
4. A person can see what an exchange has cost so far, while it is happening,
   not only afterwards.
5. Reaching a limit is visible and explained, never silent. Stopping is
   announced; so is being close to stopping.
6. A person can stop an exchange, or all exchanges, immediately and without
   ambiguity.

## Not prescribed

Whether the limit is a hop count, a budget, a rate, a deadline, or several;
what the defaults are; whether limits are per-exchange, per-agent or global;
what happens to a message that is refused - dropped, parked, or handed to a
person.
