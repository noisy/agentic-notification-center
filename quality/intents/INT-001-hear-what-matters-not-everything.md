# INT-001 - I hear what matters, not everything that was said

- actor: owner / any person whose agents are working
- source: owner, 2026-09-05, while two agents were exchanging design messages
  through a file on his desk: "for sure I don't want to be read everything out
  loud."
- intent: **I want to know what my agents are doing without having their
  conversation read to me.**

Rationale: the moment several agents work together, the volume of what they
send each other exceeds what a person can listen to, by an order of magnitude
and immediately. Speaking all of it is not thoroughness, it is a denial of
service against the one participant who cannot skim. But the opposite failure
is worse: agents working silently on someone's machine, and the person who
owns the work discovering the outcome afterwards. Attention is the scarce
resource here, not bandwidth, and it belongs to the person.

## Success conditions

1. Every item carries something short enough to be spoken and something
   complete enough to be acted on, and they are not required to be the same
   thing.
2. Only the short form is ever eligible to be spoken. Nothing can cause a
   diff, a file, a stack trace or a structured payload to be read aloud.
3. An item can be delivered to an agent while being spoken to nobody. This is
   the normal case, not an exception.
4. A person can ask what has been happening and get an answer proportionate to
   how long they were away - twenty exchanges become a sentence, not twenty
   sentences.
5. Nothing that a person needs in order to intervene is only ever available as
   speech. Speech is a notification, never the only record.
6. A person can raise or lower how much they hear, at any time, without
   changing what agents send each other.

## Not prescribed

How the short form is produced - written by the sender, generated later, or
both; what voice, language or phrasing is used; whether a summary is spoken,
shown, or both; how "how long they were away" is measured; whether silence is
the default. The one thing fixed here is that being delivered and being heard
are separate decisions about the same item.
