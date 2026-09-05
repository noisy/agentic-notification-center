# INT-007 - Installing this does not take a hook away from my other tools

- actor: owner / anyone installing this alongside tools they already use
- source: owner, 2026-09-05: "if we are taking over one specific hook which
  cannot be reproduced, it would be really polite for other tools to give them
  something instead." Raised while noisy-coding's own stop hook was holding a
  turn open for an hour.
- intent: **I want to install this without losing the ability to run my own
  hooks, or anybody else's, on the same events.**

Rationale: hook slots are shared ground. Most harnesses will run several hooks
on one event, so mere registration is not scarce - but BEHAVIOUR is. A hook
that blocks a turn, holds it open, or decides whether it continues cannot
meaningfully coexist with a second hook doing the same thing: two owners of
one decision is not a configuration, it is a race. A tool that takes such a
slot has taken something from everyone else on the machine, and taking it
silently is the part that is not acceptable. Whoever holds it owes the others
a way through.

## Success conditions

1. Installing this never removes, rewrites or disables a hook a person already
   had. What was there still runs.
2. Where this must own an exclusive decision, other participants can still be
   invoked, receive the same information, and have their outcome respected -
   not merely be allowed to observe.
3. A person can see which hooks are installed, who owns each exclusive
   decision, and in what order things run.
4. Uninstalling returns the machine to the state it was in, including hooks
   this had been relaying to.
5. A participant that fails, hangs or is slow cannot take the others down with
   it, and the failure is attributed to it by name.
6. Conflicting demands on one exclusive decision are resolved by a stated rule
   a person can read and change, never by whichever tool was installed last.

## Not prescribed

Whether relaying is configuration, discovery or a registration call; the
ordering rule; how a hung participant is bounded; whether other tools must
know they are being relayed to; which decisions are exclusive on any given
harness - that is a property of the harness, not of this.
