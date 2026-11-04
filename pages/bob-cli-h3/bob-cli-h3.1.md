# Bead: bob-cli-h3.1 — bob-cli: capture-complete --closed-tasks for task\_goto

[Bead Pages](../README.md) / [bob-cli-h3](README.md) / bob-cli-h3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.180](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.180.md) · **Assignee:** `bob-cli-h3.1` · **Size:** medium
**Created:** 2026-11-04 11:50:53 EST · **Closed:** 2026-11-04 12:15:35 EST
**Plan:** [202611/goto\_completed\_toggle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/goto_completed_toggle.md)

## Description

bob: add the -C/--closed-tasks flag and append newest-first closed rows from the vault catalog to task_goto, with tests and docs.

## Notes

[2026-11-04T17:15:18Z · bob-cli-h3.1] VERIFIED: capture-complete -C/--closed-tasks for task_goto. Open rows unchanged without flag (byte-identical shape: note_kind present, no closed/group-completed). With flag: 8 open + 5 closed (Shipped 2026-10-03, Ref done 2026-09-25, Canceled 2026-09-20, then undated Old fix, Dropped idea), group completed, locator route, no note_kind, scheduled/pomodoro null, closed date present. Query filters closed with open-first. task_link ignores flag. Human shows closed date. Gates: cargo fmt clean, clippy exit 0, cargo test lib 4967 pass, cli capture 1623 pass, task_goto 15 pass. Real-vault (athena debug): open 0.137s/557 rows, closed 1.5s/4381 rows (3824 completed), wikilink_task 1.24s for comparison — near catalog cost. docs: capture.md + reference regenerated, lint ok.

[2026-11-04T17:15:22Z · bob-cli-h3.1] PROPOSED FOLLOW-UP: just docs-check / just docs-gen generated-drift fails on sase/memory/glossary/task-merge.md missing front matter (file untouched from HEAD; prior beads bob-cli-h0.1/h0.2 record clean-tree reproduction); lint passes and cli reference was regenerated.

[2026-11-04T17:15:35Z · bob-cli-h3.1] Closed after verifying -C/--closed-tasks: lib 4967 pass, cli capture 1623 pass, task_goto 15 pass, fmt/clippy clean, real-vault closed 1.5s vs catalog 1.24s debug; docs reference regenerated (docs-check generated-drift failure is pre-existing task-merge front matter, tracked).

## Dependencies

- **Blocks:** [bob-cli-h3.2](bob-cli-h3.2.md) ◐ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h3.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h3.1/README.md) | [bob-cli-h3.1](bob-cli-h3.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f54a352`](https://github.com/bobs-org/bob-cli/commit/f54a352c06ed32f8d1e954eef74108eaa79f4fa5) | feat(capture): add capture-complete -C/--closed-tasks for task\_goto | [bob-cli-h3.1](bob-cli-h3.1.md) | 2026-11-04 12:16:54 EST |
