# Bead: bob-cli-as.6 — Counted and Task Link keep sessions with one combined prompt

[Bead Pages](../README.md) / [bob-cli-as](README.md) / bob-cli-as.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.55.linker.w2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.55.linker.w2.md) · **Assignee:** `bob-cli-as.6` · **Size:** medium
**Created:** 2026-10-23 08:24:13 EDT · **Closed:** 2026-10-23 10:49:43 EDT
**Plan:** [202610/rotten\_log.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/rotten_log.md)

## Description

keep-batches: give counted N<Alt+F> and Task Link sessions one prompt that shows a Keep reason field and/or a Work summary field, and write one entry per counted target across notes with honest refusals.

## Notes

[2026-10-23T14:46:37Z · bob-cli-as.6] PROPOSED FOLLOW-UP: Investigate bob-plugins npm test failures already tracked by bob-cli-6v, bob-cli-3w, and bob-cli-7i — clean bob-plugins HEAD 973acea reproduces four unblocked-glyph failures, the stage-ranker 16 ms assertion at 20.53 ms, and forward conversion retaining BLOCKS [[Work_ship#^prj]]; the same six failures reproduce on this phase tree.

[2026-10-23T14:49:43Z · bob-cli-as.6] Implemented combined Work summary/Keep reason prompts for counted source-note and Task Link batches, per-note deduplicated Rotten Log entries with grouped planning, stale-note rechecks, and partial-rollback reporting. Verified focused tests (91/91), npm run validate (7/7 plugins), npm run docs:check (all implemented gates; documentation tests 447 passed, 1 skipped), and bob plugins sync (2 files copied). Full npm test still has 6 failures reproduced on clean HEAD 973acea and tracked by bob-cli-6v, bob-cli-3w, and bob-cli-7i; recorded as proposed follow-up.

## Dependencies

- **Depends on:** [bob-cli-as.5](bob-cli-as.5.md) ✓ · ⧖ 2026-10-23
- **Blocks:** [bob-cli-as.7](bob-cli-as.7.md) ◐ · ⧖ 2026-10-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-as.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-as.6/README.md) | [bob-cli-as.6](bob-cli-as.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b8ef471`](https://github.com/bobs-org/bob-plugins/commit/b8ef4710a70910a4183a8bceffbea65bd4b0d269) | feat(navigation): log counted keeps across task batches | [bob-cli-as.6](bob-cli-as.6.md) | 2026-10-23 10:50:44 EDT |
