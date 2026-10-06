# Bead: bob-cli-4l.5 — Hints, docs, README, decision record, and rollout

[Bead Pages](../README.md) / [bob-cli-4l](README.md) / bob-cli-4l.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0d.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0d.linker.w0.md) · **Assignee:** `bob-cli-4l.5` · **Size:** small
**Created:** 2026-10-06 07:01:41 EDT · **Closed:** 2026-10-06 07:50:21 EDT
**Plan:** [202610/review\_walk\_answer\_auto\_advance.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/review_walk_answer_auto_advance.md)

## Description

copy-docs-record: fix the PRE/POST/lane action hints in ledger-tools and the nav fallback. Update bob-cli `docs/freshness.md` §6/§13, getting-started, task-dependencies §9 (nav api v3), the projects Task Card note, and the bob-plugins README. Write the accepted decision record through /sase_memory_write, then run the full test suite and `bob plugins sync`, and hand Bryan a manual smoke checklist.

## Notes

[2026-10-06T11:50:14Z · bob-cli-4l.5] Manual smoke checklist for Bryan: Vim normal mode on a same-note landing and a cross-note landing, for each of Ctrl+Enter, Alt+N, Ctrl+Shift+Enter (with and without a block ID), a Task Card priority commit, Task Card x, and Ctrl+Shift+M; the last row before POST with Ctrl+Enter (stays, shows ]s arrow POST hint); a double Ctrl+Enter (second swallowed); Alt+F stays; <C-o> after an auto-advance returns to the answered row.

[2026-10-06T11:50:21Z · bob-cli-4l.5] Hints fixed in ledger-tools 120 + nav 480 fallback (PRE/POST Ctrl+Enter, lanes Ctrl+Alt+F keep); tests updated; ledger 1.29.2, nav 2.6.1. README versions + api v3 + gesture rows. Docs: freshness §6/§13, getting-started, task-deps §9 api v3 + reviewWalk, projects Task Card. Decision record answering-advances-the-walk published via sase memory init. Verified: npm run build clean, full suite 1863 pass 0 fail, bob plugins sync ok (2 copied). Epic-symbols clean. Smoke checklist left as a bead note.

## Dependencies

- **Depends on:** [bob-cli-4l.2](bob-cli-4l.2.md) ✓ · ⧖ 2026-10-06
- **Depends on:** [bob-cli-4l.3](bob-cli-4l.3.md) ✓ · ⧖ 2026-10-06
- **Depends on:** [bob-cli-4l.4](bob-cli-4l.4.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-4l.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-4l.5/README.md) | [bob-cli-4l.5](bob-cli-4l.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`756c4fc`](https://github.com/bobs-org/bob-cli/commit/756c4fc74959a644d8b90edab8502aea342320fc) | docs(walk): publish answering-advances-the-walk decision and update review docs | [bob-cli-4l.5](bob-cli-4l.5.md) | 2026-10-06 07:52:22 EDT |
