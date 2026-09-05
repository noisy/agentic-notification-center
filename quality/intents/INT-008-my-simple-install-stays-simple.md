# INT-008 - The program that uses this stays as easy to install as it was

- actor: owner / the maintainer of any program that adopts this
- source: owner, 2026-09-05, on noisy-coding as the first adopter: "we want to
  keep the ability to just install the desktop version with super simple
  installation... maybe it should also be a library, I'm not sure."
- intent: **I want a program that uses this to remain a single, ordinary
  install for its users, who should not have to know this exists.**

Rationale: a desktop application that starts by asking a person to install and
run a second service has lost most of the people it was for. The value of an
attention layer is realised by ordinary users who will never read its README,
and any adoption cost lands on the adopting program's install instructions,
where it is fatal. At the same time a person running several tools should not
end up with several copies of the same bus, each holding a different half of
the truth.

## Success conditions

1. A program can adopt this without adding a separate installation step for
   its users.
2. Nothing about this appears in the adopting program's setup instructions,
   its prerequisites, or its error messages during normal use.
3. Several programs on one machine converge on one shared bus rather than
   each running their own, without any of them having been configured to.
4. The first program to need it can bring it up, and a program that finds it
   already running uses it as it is.
5. If it is absent or fails to start, the adopting program degrades to what it
   could do without it, and says so once, rather than failing.
6. Adopting this does not force the adopting program's own architecture -
   language, packaging and process model stay the adopter's choice.

## Not prescribed

Whether this is a library, a service, both, or a library that starts a
service; how instances discover each other; who owns the lifecycle; how
versions between an adopter and a running bus are reconciled.
