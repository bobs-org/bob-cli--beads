# Bead: bob-cli-q4.6 — Capture settles every note it touches

[Bead Pages](../README.md) / [bob-cli-q4](README.md) / bob-cli-q4.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fw.md) · **Assignee:** `bob-cli-q4.6` · **Size:** medium
**Created:** 2026-11-25 08:51:35 EST · **Closed:** 2026-11-25 10:39:41 EST
**Plan:** [202611/better\_o\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/better_o_gesture_settle.md)

## Description

capture-settle: run `settle_note` at the capture choke point after type agreement and before the trackers finish. Forward the task-block tracker and `items[].result.line` through the line map so dry-run and commit stay byte-identical and Mac Capture's Open lands on the post-settle line, with no Swift changes.

## Notes

[2026-11-25T15:39:41Z · bob-cli-q4.6--1] Implemented capture-time settling before tracker finalization; forwarded settled task and parent lines. Verified cargo test --test cli note_bullets_compose passed, cargo fmt --check passed, and epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-q4.13](bob-cli-q4.13.md) ◐ · ⧖ 2026-11-25
- **Depends on:** [bob-cli-q4.3](bob-cli-q4.3.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.6.md) | [bob-cli-q4.6](bob-cli-q4.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`007ef5e`](https://github.com/bobs-org/bob-cli/commit/007ef5ed819595338ad7f629e660c43fcf2b496f) | feat(capture): settle touched notes before reporting lines | [bob-cli-q4.6](bob-cli-q4.6.md) | 2026-11-25 10:40:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.6.1.3][1] | Capture-settle likely caused project_note fixture drift; check if already noted | 1 |
| read-by | [agent:bob-cli-q4.6--1][2] | Need current phase scope, design file, decisions, and prior notes before closing | 1 |
| read-by | [agent:bob-cli-q4.7][3] | check capture-settle state | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ph.6.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.6.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.7/README.md

<!-- sase:referenced-by:end -->
