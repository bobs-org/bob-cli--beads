# Bead: bob-cli-my.3 — Refuse offset starts before the current ledger day

[Bead Pages](../README.md) / [bob-cli-my](README.md) / bob-cli-my.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-mr.land--2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.land.md) · **Assignee:** `bob-cli-my.3` · **Size:** medium
**Created:** 2026-11-17 19:17:52 EST · **Closed:** 2026-11-17 21:35:37 EST
**Plan:** [202611/backlog\_triage\_t2.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t2.md)

## Description

midnight-dating: refuse past-offset starts before today while preserving valid overnight ends, and close bob-cli-h1.

## Notes

[2026-11-18T02:35:07Z · bob-cli-my.3] PROPOSED FOLLOW-UP: just docs-check reports generated drift in docs/reference/glossary.md (run just docs-gen) identically on the clean base tree without this phase changes; pre-existing, unrelated to midnight-dating.

[2026-11-18T02:35:37Z · bob-cli-my.3] Midnight-dating done: compute_pomodoro_start_range refuses start_raw<0 before any edit (usage error with wrapped HHMM + max offset from same rounded anchor, e.g. =-3 at 00:05 teaches =-1); end wrap and +later future starts preserved. Tests: new capture_pomodoro_start_refuses_past_midnight_offset (bare/named/task-link/chain, boundary/just-too-large/zero/large/overflow, valid chain) plus start/MEET/past suites pass; just check green. Docs updated in docs/capture.md. Closed bob-cli-h1 with evidence. Pre-existing docs-check glossary drift recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-my.2](bob-cli-my.2.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-my.4](bob-cli-my.4.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-my.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-my.3/README.md) | [bob-cli-my.3](bob-cli-my.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`97f844c`](https://github.com/bobs-org/bob-cli/commit/97f844caf4a942f275dc22336136834a94ed2cfa) | fix(capture): refuse past-midnight Pomodoro offset starts | [bob-cli-my.3](bob-cli-my.3.md) | 2026-11-17 21:37:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-my.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-my.3/README.md

<!-- sase:referenced-by:end -->
