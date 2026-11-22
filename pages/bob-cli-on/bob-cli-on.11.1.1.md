# Bead: bob-cli-on.11.1.1 — Carry a requirement through the navigation split API

[Bead Pages](../README.md) / [bob-cli-on.11.1](bob-cli-on.11.1.md) / bob-cli-on.11.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.md) · **Assignee:** `bob-cli-on.11.1.1` · **Size:** medium
**Created:** 2026-11-22 14:59:30 EST · **Closed:** 2026-11-22 15:41:01 EST
**Plan:** [202611/obsidian\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_requirement_close_card.md)

## Description

carry_api: extend the Task Split twin through SP50, publish taskSplit v1, and route Ctrl+Shift+T on requirement lines through guarded carry with jump history.

## Notes

[2026-11-22T20:40:42Z · bob-cli-on.11.1.1] PROPOSED FOLLOW-UP: full-suite npm test unit flake in scripts/test-ledger-tools-event-link-times.cjs 25ms budget (subtests 2080/2089 vary run to run; file passes 23/23 in isolation on this tree and on base; sibling precedent bob-cli-on.11.1.2 noted the same pattern for frees-marks)

[2026-11-22T20:41:01Z · bob-cli-on.11.1.1] carry_api landed: taskSplit v1 with carryReq, guarded destination-first persistence, and Ctrl+Shift+T req routing. Verified: SP1-SP51 vectors byte-identical (Rust-equivalent comparison incl. req_depth/moves/stubs), vector/gesture/carry-api suites 44/44 green, npm build+build:check+docs:gen+docs:check+inventory:check green, full npm test 8746 pass with 1 known load-flaky 25ms timing subtest (passes 23/23 in isolation; recorded as PROPOSED FOLLOW-UP), deployed to vault via descendant sync (no -F). No memory, bob-cli, Cargo, or CHANGELOG edits.

## Dependencies

- **Blocks:** [bob-cli-on.11.1.4](bob-cli-on.11.1.4.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.11.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.1/README.md) | [bob-cli-on.11.1.1](bob-cli-on.11.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@1e38521`](https://github.com/bobs-org/bob-plugins/commit/1e3852184dc6c1b780d6e9729071c5ba448171e5) | feat(task-split): add req-carry planner, guarded persistence and carry API | [bob-cli-on.11.1.1](bob-cli-on.11.1.1.md) | 2026-11-22 15:41:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.11.1.2][1] | Need sibling phase scope to see if it also deploys cycler/nav and should wait | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.2/README.md

<!-- sase:referenced-by:end -->
