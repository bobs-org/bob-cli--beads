# Bead: bob-cli-42.3 — Render the compact Task Card and its accessible visual states

[Bead Pages](../README.md) / [bob-cli-42](README.md) / bob-cli-42.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.05.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.05.linker.w0.md) · **Assignee:** `bob-cli-42.3` · **Size:** medium
**Created:** 2026-10-03 16:27:19 EDT · **Closed:** 2026-10-03 17:25:08 EDT
**Plan:** [202610/ctrl\_shift\_p\_task\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_shift_p_task_card.md)

## Description

card-view: add the task header, recommendation timeline, priority strip, stable action rows, theme-native styles, and permanent classic search mode.

## Notes

[2026-10-03T21:24:54Z · bob-cli-42.3] PROPOSED FOLLOW-UP: Live vault bob-navigation-hotkeys is 1.72.0 with FreshnessRefreshSummaryModal; this phase ships 1.71.1 Task Card view — withheld `bob plugins sync` into ~/bob to avoid downgrading that lineage. Disposable --bob-dir /tmp/bob-task-card-sync-p5Lq copied manifest/main.js/styles.css byte-matching source. Land/sync after 1.72.0 is reconciled with this source.

[2026-10-03T21:25:08Z · bob-cli-42.3] Card-view only: BulletPropertyPickerModal opt-in taskCard renders header/banner/priority strip/stable rows/disabled reasons/More/footer/disclosures/close from planTaskCard with no render-time roll/write. Compact bob-task-card-modal + shared bob-key-card tokens with decay card; vault Depends on uses bob-task-card-wide. 11 view tests + 7 model tests pass (classic width, search Back restore, child-note/task-move/Pomodoro keep bob-cnp-modal, missing freshness API, no-rec/cancel/mixed/error/long-title). epic-symbols: none leftover. Live ~/bob sync withheld (vault 1.72.0 vs source 1.71.1); disposable vault byte-matched.

## Dependencies

- **Depends on:** [bob-cli-42.2](bob-cli-42.2.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-42.4](bob-cli-42.4.md) ◐ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-42.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-42.3/README.md) | [bob-cli-42.3](bob-cli-42.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c0ff974`](https://github.com/bobs-org/bob-plugins/commit/c0ff9742efb7c49e948d61f50a06383948acb952) | feat(navigation-hotkeys): render compact Task Card view | [bob-cli-42.3](bob-cli-42.3.md) | 2026-10-03 17:31:33 EDT |
