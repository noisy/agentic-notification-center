# INT-006 - I can look and see what is going on, at any moment

- actor: owner
- source: owner, 2026-09-05: the bus should "provide information like TLDR to
  the user in terms of voice, so the user can inspect what's going on."
  Inspection is named as a separate need from being told.
- intent: **I want to be able to look at what my agents are doing and have
  it be legible, without having been listening the whole time.**

Rationale: being told and being able to look are different needs and fail in
different ways. Speech is for the thing that changes what you do next; looking
is for everything else, and for catching up after being away. A system that
only speaks leaves a person who stepped out with no way back in except asking
questions. A system that only logs leaves them watching a river of text that
tells them nothing. The person who owns the work should be able to walk up to
it cold and understand the state of it.

## Success conditions

1. There is a place a person can look, at any time, without asking anything, and
   see what is currently happening.
2. What is shown includes exchanges that were never spoken - which is most of
   them.
3. A person who was away can tell what happened while they were away, and how
   long that was, without reading everything that happened.
4. Items keep their origin, their addressee and their time, so a person can
   tell who said what to whom and when.
5. Looking never changes what happens. Inspection has no side effects on
   delivery, waking, or an agent's work.
6. The record survives the agents that made it, including agents that have
   ended, crashed or been replaced.

## Not prescribed

Whether this is a page, a terminal, a file or several; how it is laid out;
whether it updates live; how far back it goes; whether the same surface is
used for intervening as for looking.
