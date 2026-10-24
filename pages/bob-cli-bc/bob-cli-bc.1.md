# Bead: bob-cli-bc.1 — Lossless name reuse and the exact-name literal

[Bead Pages](../README.md) / [bob-cli-bc](README.md) / bob-cli-bc.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2c.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2c.linker.w1.md) · **Assignee:** `bob-cli-bc.1` · **Size:** medium
**Created:** 2026-10-24 07:52:22 EDT · **Closed:** 2026-10-24 09:18:44 EDT
**Plan:** [202610/pomodoro\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_themes.md)

## Description

lossless: fix bob-cli-bb so reusing a completed name keeps its spelling, and add the `#"NAME"` exact-name literal to every capture name position.

## Notes

[2026-10-24T13:18:20Z · bob-cli-bc.1] PROPOSED FOLLOW-UP: docs-check published-URL obligations for /pomodoro-themes/ and /reference/cli/themes/ fail identically on the clean base tree (verified via stashed docs/capture.md); those pages ship with later catalog/CLI phases, not lossless

[2026-10-24T13:18:44Z · bob-cli-bc.1] Lossless reuse + exact-name literal done: just check green (fmt, clippy gate, 18 test suites incl. 3251 lib + 9 exact_name + 3 assembly regressions); live scratch probes: =#"DEEP WORK" and @inbox_t:foo1#"DEEP WORK" create/link DEEP WORK, =#"BOB" creates BOB with BOB BUILD open, SASE V18 vs SASE-V18 distinct, unterminated literal incomplete; docs/capture.md updated (grammar, named-start, link, parse spans, complete, rewrite, zsh quoting) with docs-gen clean; docs-check URL failure reproduces on clean base, recorded as PROPOSED FOLLOW-UP

## Dependencies

- **Blocks:** [bob-cli-bc.4](bob-cli-bc.4.md) ◐ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bc.5](bob-cli-bc.5.md) ◐ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bc.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.1/README.md) | [bob-cli-bc.1](bob-cli-bc.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`32e0e8f`](https://github.com/bobs-org/bob-cli/commit/32e0e8fa6b679793c7cc27b844f26fe285a3a254) | feat(capture): support exact-name literals with docs and regression tests | [bob-cli-bc.1](bob-cli-bc.1.md) | 2026-10-24 09:36:57 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bc.1][1] | Need the phase scope and design file | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bc.1/README.md

<!-- sase:referenced-by:end -->
