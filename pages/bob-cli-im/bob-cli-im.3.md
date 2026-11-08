# Bead: bob-cli-im.3 — Refuse operator-only bodies after a link start, teaching the glued spelling

[Bead Pages](../README.md) / [bob-cli-im](README.md) / bob-cli-im.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5x.linker.w0.md) · **Assignee:** `bob-cli-im.3` · **Size:** small
**Created:** 2026-11-08 05:50:21 EST · **Closed:** 2026-11-08 09:15:56 EST
**Plan:** [202611/start\_timing\_later\_offset.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/start_timing_later_offset.md)

## Description

link_body: an `@route:id[#name]=<X>` item whose remaining text is only session-operator tokens (`@foo:bar= ++3`) is refused instead of creating a task titled `++3`; a single `++N` body teaches the folded spelling (`@foo:bar=+3`, `@foo:bar=fix2+`), and the `^route:id=<X> ++N` near miss teaches the same fold. Bump the grammar revision and document it.

## Notes

[2026-11-08T14:15:56Z · bob-cli-im.3] Implemented operator-only link-start body refusals with operator-range diagnostics and folded ++[N] hints; verified just check, just docs-gen, just docs-check, and the focused no-write/editor tests.

## Dependencies

- **Depends on:** [bob-cli-im.2](bob-cli-im.2.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-im.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-im.3.md) | [bob-cli-im.3](bob-cli-im.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`572ce97`](https://github.com/bobs-org/bob-cli/commit/572ce974c9d933e8bb0547418fd421d22e2957b3) | feat(capture): refuse operator-only link-start bodies | [bob-cli-im.3](bob-cli-im.3.md) | 2026-11-08 09:42:54 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-im.3--1][1] | Need the current phase state after verification completion was rejected | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-im.3.md

<!-- sase:referenced-by:end -->
