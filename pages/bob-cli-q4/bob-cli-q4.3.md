# Bead: bob-cli-q4.3 — One pure Rust settle\_note that reconcile composes

[Bead Pages](../README.md) / [bob-cli-q4](README.md) / bob-cli-q4.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fw.md) · **Assignee:** `bob-cli-q4.3` · **Size:** medium
**Created:** 2026-11-25 08:51:35 EST · **Closed:** 2026-11-25 10:16:53 EST
**Plan:** [202611/better\_o\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/better_o_gesture_settle.md)

## Description

settle-core: extract reconcile's note-local subset (the local future-schedule Blocked rule plus status groups and badges for eligible notes) as a pure `settle_note` with a line map. Reconcile composes it with byte-identical output. Add a writer helper and Rust-owned settle vectors for the plugin twin.

## Notes

[2026-11-25T15:16:40Z · bob-cli-q4.3--1] PROPOSED FOLLOW-UP: Run final verification on the current origin/master base before land review. The just check failures and clean HEAD reproduction at 8f88a52 are the 17 xelatex preamble failures caused by meeting.lua placing \AtBeginDocument after \begin{document}; already tracked by bob-cli-pw note #4 and repaired by origin/master commit f47055da (this checkout is three commits behind).

[2026-11-25T15:16:53Z · bob-cli-q4.3--1] Implemented settle_note, reconcile composition, writer helper, Rust vectors, parity coverage, and docs. Targeted settle vectors and reconcile composition passed; just check had 8088 passing and 17 failing xelatex tests, reproduced on clean HEAD 8f88a52. The preamble defect is already tracked by bob-cli-pw note #4 and fixed by origin/master f47055da. epic-symbols reported none.

## Dependencies

- **Blocks:** [bob-cli-q4.13](bob-cli-q4.13.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.6](bob-cli-q4.6.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.7](bob-cli-q4.7.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.8](bob-cli-q4.8.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.3.md) | [bob-cli-q4.3](bob-cli-q4.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9395683`](https://github.com/bobs-org/bob-cli/commit/9395683818ef4a11527fda82c5290e20ef6aebe6) | feat(task): add pure note settle helper | [bob-cli-q4.3](bob-cli-q4.3.md) | 2026-11-25 10:18:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.3--1][1] | Need the phase scope, design file, notes, and decisions before completing verification | 1 |
| read-by | [agent:bob-cli-q4.7][2] | check settle-core deliverable | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.3.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.7/README.md

<!-- sase:referenced-by:end -->
