# Agentic Notification Center

A message bus and an attention layer for AI coding agents.

Agents talk to each other. You hear the summary, not the traffic.

## The problem

An agent working alone is easy to follow: it says what it did, you listen.
Several agents working together are not. They need to exchange far more than
a person wants to hear - diffs, findings, corrections, whole files - and the
moment that exchange is routed through a human it stops being collaboration
and becomes dictation.

Reading all of it aloud is unusable. Reading none of it aloud leaves the
person who owns the work with no idea what is happening on their own machine.

## What this is

One stream that carries everything an agent should know about - another
agent's message, a finished pipeline, a new follower, a failing test, a
person speaking - and decides two separate questions about each item:

1. **Who needs to act on it, and how urgently?** Wake them now, wait until
   their current work ends, or leave it for review.
2. **Should a human hear about it, and as what?** The event itself, a
   summary of twenty like it, or nothing at all.

Those are deliberately not the same question. Most of what agents send each
other is never spoken. Some of what a person needs to hear was never sent to
them.

## Status

Early. The intents are being written before the implementation - see
`quality/intents/`. Nothing here is stable.

## How this is specified

`quality/intents/` describes what someone wants and why, in their terms, with
success conditions and an explicit list of what is deliberately left open.
Technical proposals live separately in `docs/`, and an intent is never
allowed to depend on one - the intent outlives the mechanism chosen to serve
it.

## Origin

Extracted from [noisy-coding](https://github.com/noisy/noisy-coding), where
the voice daemon had already grown two thirds of a notification centre by
accident: a queue, delivery into a running agent, waking an idle one, and
priorities. It was missing an input for anything that was not a human voice.
