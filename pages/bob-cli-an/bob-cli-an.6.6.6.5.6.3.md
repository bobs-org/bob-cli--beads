# Bead: bob-cli-an.6.6.6.5.6.3 — Persist project anchors despite a concurrent frontmatter write

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6](bob-cli-an.6.6.6.5.6.md) / bob-cli-an.6.6.6.5.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.3` · **Size:** medium
**Created:** 2026-10-24 09:36:39 EDT · **Closed:** 2026-10-24 10:46:43 EDT
**Plan:** [202610/backlog\_batch6\_color\_quote\_walk\_blocks\_shift\_promotion\_race\_mac\_panel\_ci.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch6_color_quote_walk_blocks_shift_promotion_race_mac_panel_ci.md)

## Description

promotion-anchor-race: resolve bob-cli-79 so that promoting a task with converted child bullets persists its project anchors when bob-project-tasks or Templater touch the new note after the seed write.

## Notes

[2026-10-24T14:46:24Z · bob-cli-an.6.6.6.5.6.3] Baseline reproduced from bob-cli-79: concurrent task_count/open_task_count frontmatter made the second whole-file preimage check refuse, retaining the source task. Implemented latest-content anchor rebasing keyed to the converted task-line preimages, with separate closed-editor and open-editor paths; edited target lines and ID collisions remain guarded. Focused promotion harness 13/13, npm run validate, final npm test 3560/3560, and npm run docs:check 447 passed / 1 expected skip. Bumped bob-navigation-hotkeys 2.56.3 -> 2.56.4, built, synced with bob plugins sync, and verified installed manifest 2.56.4 plus source/deployed main.js match. No remaining phase work; source task bob-cli-79 remains open for the epic lander to close.

[2026-10-24T14:46:43Z · bob-cli-an.6.6.6.5.6.3] Verified latest-content promotion anchor rebasing with closed and open editor frontmatter races; conflicting task edits still refuse. Focused harness 13/13, npm run validate, npm test 3560/3560, docs check 447 passed with 1 expected skip. Deployed bob-navigation-hotkeys 2.56.4 and verified installed manifest and main.js.

## Dependencies

- **Depends on:** [bob-cli-an.6.6.6.5.6.2](bob-cli-an.6.6.6.5.6.2.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.3/README.md) | [bob-cli-an.6.6.6.5.6.3](bob-cli-an.6.6.6.5.6.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3a7368a`](https://github.com/bobs-org/bob-plugins/commit/3a7368a1c8cc94bfde9fe6c5ac217c16f5bf6e49) | fix(navigation): preserve project promotion anchors across frontmatter writes | [bob-cli-an.6.6.6.5.6.3](bob-cli-an.6.6.6.5.6.3.md) | 2026-10-24 10:47:21 EDT |
