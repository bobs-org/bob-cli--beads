# Bead: bob-cli-bk.1 — Detect inbox route candidates and refuse without a choice

[Bead Pages](../README.md) / [bob-cli-bk](README.md) / bob-cli-bk.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.a9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.a9.md) · **Assignee:** `bob-cli-bk.1` · **Size:** medium
**Created:** 2026-10-24 14:00:27 EDT · **Closed:** 2026-10-24 14:57:15 EDT
**Plan:** [202610/capture\_inbox\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_inbox_routing.md)

## Description

route-detect: bob capture finds existing inbox tasks whose checkbox the batch changes, reports them with route destinations in `inbox_route`, and refuses write-free under hidden `--require-inbox-route-choice`.

## Notes

[2026-10-24T18:56:55Z · bob-cli-bk.1] PROPOSED FOLLOW-UP: Ask whether to authorize a memory decision record for inbox task routing; this phase followed memory_decision_record=no.

[2026-10-24T18:57:15Z · bob-cli-bk.1] Implemented inbox route candidate detection and the hidden write refusal guard; documented the JSON/human output and IR vectors. Focused planner, destination, and CLI routing tests passed, as did cargo test --no-run and just docs-check. just check formatting and Clippy passed, but its library and CLI suites have 1 and 5 failures respectively; each reproduces with the same failure on clean base commit 2da7bbef. git diff --check passed; no epic-symbol entries remain.

## Dependencies

- **Blocks:** [bob-cli-bk.2](bob-cli-bk.2.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bk.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bk.1/README.md) | [bob-cli-bk.1](bob-cli-bk.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bb52dd0`](https://github.com/bobs-org/bob-cli/commit/bb52dd0ab1c5d947a84b2c98f6e29620c7a3e7ff) | feat(capture): detect inbox route choices | [bob-cli-bk.1](bob-cli-bk.1.md) | 2026-10-24 14:58:27 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bk.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bk.1/README.md

<!-- sase:referenced-by:end -->
