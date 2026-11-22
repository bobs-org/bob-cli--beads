# Bead: bob-cli-oz.2 — block-id-prompt api.taskLinks v1: prose detector, ranked session, and safe ID naming

[Bead Pages](../README.md) / [bob-cli-oz](README.md) / bob-cli-oz.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.ff](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ff.md) · **Assignee:** `bob-cli-oz.2` · **Size:** medium
**Created:** 2026-11-21 17:39:51 EST · **Closed:** 2026-11-22 00:21:09 EST
**Plan:** [202611/prompt\_task\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prompt_task_links.md)

## Description

bip-task-api: expose the existing (( engine as api.taskLinks v1. It adds the prose fieldAt detector replaying the shared vectors, a snapshot session with ranked rows, guards (including subjects) and indexing progress, and an editor-free validate/name write via vault.process or the open editor.

## Notes

[2026-11-22T04:58:12Z · bob-cli-oz.2] PROPOSED FOLLOW-UP: Fix the published-URL docs-check false positive for the Podcastindex namespace URL at src/native/highlights_ref/podcast/feed.rs:70 — bob-cli-os note #1 tracks this exact failure and note #2 confirms it reproduces identically on a clean tree; this phase docs-check reproduced it.

[2026-11-22T05:20:41Z · bob-cli-oz.2--2] PROPOSED FOLLOW-UP: Record baseline Ledger Tools timing failures in existing trackers bob-cli-km and bob-cli-io. Clean-base bob-plugins npm test (monitor gete0w5b2qb4, clean-base worktree) reproduced event-link-times at scripts/test-ledger-tools-event-link-times.cjs:1069 (90.6 ms vs 25 ms) and frees-marks at scripts/test-ledger-tools-frees-marks.cjs:481 (87 ms vs 25 ms); this matches current-phase run g1zy1a0hhg1m (36.2 ms and 255 ms) and the existing full-suite timing trackers. The clean-base run had one additional SV fixture ENOENT because the current bob-cli checkout lacks sase/tests/fixtures/offer_close/vectors.json; phase-tree run passed that fixture check. Neither timing test is in this phase's api.taskLinks diff.

[2026-11-22T05:21:09Z · bob-cli-oz.2--2] Completed api.taskLinks phase. Validation: npm run validate and focused picker regressions passed; phase-tree npm test failed only the two already tracked Ledger Tools 25 ms full-suite timing checks (monitor g1zy1a0hhg1m: event-link-times 36.2 ms, frees-marks 255 ms). Clean-base npm test reproduced both (monitor gete0w5b2qb4: event-link-times 90.6 ms, frees-marks 87 ms), confirming baseline failures tracked by bob-cli-km and bob-cli-io; it also had an unrelated missing offer_close/vectors.json fixture-path error absent from the phase-tree run. Added the required PROPOSED FOLLOW-UP note with evidence. sase bead epic-symbols bob-cli-oz.2 reported no leftovers. Temporary clean-base worktree removed. No sync rerun.

## Dependencies

- **Depends on:** [bob-cli-oz.1](bob-cli-oz.1.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oz.3](bob-cli-oz.3.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oz.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oz.2.md) | [bob-cli-oz.2](bob-cli-oz.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a346fd2`](https://github.com/bobs-org/bob-plugins/commit/a346fd2f3bfbae27296535fb3075c3b15b4812f3) | feat(block-id-prompt): add task links API | [bob-cli-oz.2](bob-cli-oz.2.md) | 2026-11-22 00:02:06 EST |
