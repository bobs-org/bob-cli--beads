# Bead: bob-cli-im.3 — Refuse operator-only bodies after a link start, teaching the glued spelling

[Bead Pages](../README.md) / [bob-cli-im](README.md) / bob-cli-im.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5x.linker.w0.md) · **Assignee:** `bob-cli-im.3` · **Size:** small
**Created:** 2026-11-08 05:50:21 EST
**Plan:** [202611/start\_timing\_later\_offset.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/start_timing_later_offset.md)

## Description

link_body: an `@route:id[#name]=<X>` item whose remaining text is only session-operator tokens (`@foo:bar= ++3`) is refused instead of creating a task titled `++3`; a single `++N` body teaches the folded spelling (`@foo:bar=+3`, `@foo:bar=fix2+`), and the `^route:id=<X> ++N` near miss teaches the same fold. Bump the grammar revision and document it.

## Dependencies

- **Depends on:** [bob-cli-im.2](bob-cli-im.2.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-im.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-im.3/README.md) | [bob-cli-im.3](bob-cli-im.3.md) | 0 |
