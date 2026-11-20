# Bead: bob-cli-nj.4 — bob-plugins: Rotten keep prompts and the successor inline cancel reason

[Bead Pages](../README.md) / [bob-cli-nj](README.md) / bob-cli-nj.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.f3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.f3.md) · **Assignee:** `bob-cli-nj.4` · **Size:** medium
**Created:** 2026-11-19 12:14:03 EST · **Closed:** 2026-11-19 20:07:47 EST
**Plan:** [202611/log\_reason\_recall.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/log_reason_recall.md)

## Description

rotten-and-successor: attach Rotten recall to RottenKeepReasonStage (single keep and decay-card Stay) and to the batch keep form (which gets the standard footer). Attach dense Cancel recall to the successor picker's inline reason, with a blur-commit guard. Wire noteUsed into the rotten and successor-cancel writers.

## Notes

[2026-11-20T01:07:47Z · bob-cli-nj.4--1] Implemented Rotten and successor Cancel recall. npm run build and build:check passed; focused tests passed (76). Resolved protected deploys per bob-plugins deployment guidance and successfully synced bob-navigation-hotkeys; task-status-cycler already matched. Epic-symbol check: no entries.

## Dependencies

- **Depends on:** [bob-cli-nj.2](bob-cli-nj.2.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nj.8](bob-cli-nj.8.md) ◐ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nj.4.md) | [bob-cli-nj.4](bob-cli-nj.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@7eb0685`](https://github.com/bobs-org/bob-plugins/commit/7eb0685a30c13844d7dbf2546d1709e214ed3d75) | feat(plugins): add Rotten and Cancel log recall | [bob-cli-nj.4](bob-cli-nj.4.md) | 2026-11-19 20:09:35 EST |
