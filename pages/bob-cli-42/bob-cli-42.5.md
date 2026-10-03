# Bead: bob-cli-42.5 — Add concise date input and inline scheduling reasons

[Bead Pages](../README.md) / [bob-cli-42](README.md) / bob-cli-42.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.05.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.05.linker.w0.md) · **Assignee:** `bob-cli-42.5` · **Size:** medium
**Created:** 2026-10-03 16:27:20 EDT · **Closed:** 2026-10-03 18:57:58 EDT
**Plan:** [202610/ctrl\_shift\_p\_task\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_shift_p_task_card.md)

## Description

schedule-input: extend date input with bare day offsets, unsigned units, weekdays, exact previews, inline reasons, and Shift+Enter reason skipping.

## Notes

[2026-10-03T22:57:44Z · bob-cli-42.5] PROPOSED FOLLOW-UP: GUI smoke of Task Card date input in live Obsidian — this phase verified grammar, preview, inline reason, Shift+Enter, classic isolation, and vault file parity (nav 1.75.0) in the headless harness; no interactive reload was available here.

[2026-10-03T22:57:58Z · bob-cli-42.5] Verified schedule-input: conservative typed-schedule resolver {date,reason,valid,error} (bare N, unsigned Nd/Nw/Nm, weekdays next-after-today, ISO/M-D/+Nd/w/m, inline reason after complete token+whitespace); Task Card preview row, invalid is-invalid styling, Shift+Enter blank-reason path, classic parser/serial prompt when taskCard is false. 15/15 scripts/test-navigation-task-card-schedule.cjs, npm run validate 6/6, npm test 1692/0, node --check main.js. Rebased onto origin nav 1.74.0 (N]s jumps), shipped as 1.75.0; bob plugins sync --no-pull copied manifest/main.js/styles.css with vault file parity. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-42.4](bob-cli-42.4.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-42.6](bob-cli-42.6.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-42.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-42.5/README.md) | [bob-cli-42.5](bob-cli-42.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@48f0466`](https://github.com/bobs-org/bob-plugins/commit/48f046624b448dbb90e9170244f3a0a201f66f38) | feat(navigation): add concise Task Card date input and inline reasons | [bob-cli-42.5](bob-cli-42.5.md) | 2026-10-03 18:59:07 EDT |
