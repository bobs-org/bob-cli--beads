# Bead: bob-cli-q4.2 — o and O open real siblings after the whole subtree

[Bead Pages](../README.md) / [bob-cli-q4](README.md) / bob-cli-q4.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fw.md) · **Assignee:** `bob-cli-q4.2` · **Size:** medium
**Created:** 2026-11-25 08:51:35 EST · **Closed:** 2026-11-25 09:16:19 EST
**Plan:** [202611/better\_o\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/better_o_gesture_settle.md)

## Description

open-lines: `o`/`O` on task headlines open a fresh `#task [created::]` after the whole block. Inside a status group they open at the intake end. Reqs, drawers, and notes get siblings after their subtree, and managed lines redirect to the owner's note slot. Empty scaffolds prune themselves, `Ctrl+Shift+]` refuses managed lines, and the coordination note goes on bob-cli-ph.7.

## Notes

[2026-11-25T14:15:56Z · bob-cli-q4.2] PROPOSED FOLLOW-UP: ledger-tools frees-marks 25ms budget flake — test-ledger-tools-frees-marks.cjs 200-link/2000-task build took 26ms vs 25ms budget; unrelated to open-lines, did not touch that plugin

[2026-11-25T14:16:05Z · bob-cli-q4.2] PROPOSED FOLLOW-UP: task_reqs layout.json fixture drift vs bob-cli — test-task-reqs-twin-copies.cjs and test-task-status-cycler-task-reqs-vectors.cjs fail "layout.json matches bob-cli canonical fixture"; this phase did not edit layout.json or twins 194/196

[2026-11-25T14:16:19Z · bob-cli-q4.2] Implemented cycler o/O via planOpenLine: new-task [created::] after the whole block, intake_end inside status groups with C-o jump, ^prj intake/refuse, req/drawer/note siblings after subtree, managed lines redirect through taskBlockNoteHome/EnsureNotesDrawer, empty-scaffold prune, Ctrl+Shift+] managed refuse. Unit tests cover tab+2-space headlines, req leaf/subtree, nested/drawer/managed/group/^prj/pomodoro/bank, CRLF, prune, undo, jump. E2e harness cases added. Docs 1.60.0. Deployed bob plugins sync -p task-status-cycler. Pre-existing layout.json drift and 25ms frees-marks flake recorded as follow-ups.

## Dependencies

- **Blocks:** [bob-cli-q4.12](bob-cli-q4.12.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.13](bob-cli-q4.13.md) ◐ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q4.9](bob-cli-q4.9.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.2/README.md) | [bob-cli-q4.2](bob-cli-q4.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a971285`](https://github.com/bobs-org/bob-plugins/commit/a971285b2fe70720dd0a3429512879737810120e) | feat(task-status-cycler): open real siblings with o and O | [bob-cli-q4.2](bob-cli-q4.2.md) | 2026-11-25 09:17:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.2][1] | Need the phase scope, status, and design file after compaction | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.2/README.md

<!-- sase:referenced-by:end -->
