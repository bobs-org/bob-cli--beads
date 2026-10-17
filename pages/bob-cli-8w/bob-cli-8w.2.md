# Bead: bob-cli-8w.2 — Obsidian handler that opens several notes and lands on each

[Bead Pages](../README.md) / [bob-cli-8w](README.md) / bob-cli-8w.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.8q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.8q.md) · **Assignee:** `bob-cli-8w.2` · **Size:** medium
**Created:** 2026-10-17 15:54:14 EDT · **Closed:** 2026-10-17 16:15:18 EDT
**Plan:** [202610/ctrl\_enter\_capture\_and\_open.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_enter_capture_and_open.md)

## Description

obsidian-open-uri: in bob-plugins, register a read-only `obsidian://bob-open-notes` handler in bob-navigation-hotkeys. It runs one URL at a time, waits until bob's writes are visible in Obsidian, opens the notes under the tab policy, and lands on and highlights the primary line. Also covers notices, tests, README, version bump, build, and `bob plugins sync`.

## Notes

[2026-10-17T20:15:02Z · bob-cli-8w.2--1] PROPOSED FOLLOW-UP: Fix the existing clean-base npm test failures tracked by bob-cli-6v (four unblocked-glyph tests), bob-cli-6w (Keep-count notice assertion), and bob-cli-7i (reverse project conversion BLOCKS link); the full suite also hit the known parallel-load stage-ranker timing flake tracked by bob-cli-3w (33.04 ms vs 16 ms, passing standalone). The six deterministic failures reproduced on clean HEAD.

[2026-10-17T20:15:18Z · bob-cli-8w.2--1] Verified bob-open-notes URI tests, plugin build, manifest validation, and vault sync. Full npm test has six clean-base failures tracked by bob-cli-6v, bob-cli-6w, and bob-cli-7i, plus the known standalone-passing timing flake tracked by bob-cli-3w; recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-8w.3](bob-cli-8w.3.md) ✓ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8w.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8w.2.md) | [bob-cli-8w.2](bob-cli-8w.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8w.2--1][1] | Need the phase scope, design file, prior notes, and remaining work after monitored command failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8w.2.md

<!-- sase:referenced-by:end -->
