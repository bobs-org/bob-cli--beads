# Bead: bob-cli-ak.2 — Recurrence marks in Live Preview and rendered views

[Bead Pages](../README.md) / [bob-cli-ak](README.md) / bob-cli-ak.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.28.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.28.linker.w0.md) · **Assignee:** `bob-cli-ak.2` · **Size:** medium
**Created:** 2026-10-21 08:49:59 EDT · **Closed:** 2026-10-21 09:48:02 EDT
**Plan:** [202610/gtd\_checklist\_glyphs\_and\_recurrence\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gtd_checklist_glyphs_and_recurrence_marks.md)

## Description

recurrence-marks: render each canonical, Tasks-readable `[repeat:: …]` as a quiet date-family mark (loop glyph plus spoken cadence label, exact rule in the tooltip). Adds the checklist `when done` guard, the repeat repair flag, the "Recurrence (not a date)" date-marks contract section, and the vault-format `repeat` row.

## Notes

[2026-10-21T13:47:50Z · bob-cli-ak.2] PROPOSED FOLLOW-UP: Pre-existing npm failures unchanged by this phase — unblocked-glyph x4 (tracked by bob-cli-6v), decision-card Keep counts x1 (tracked by bob-cli-6w), forward-promotion conversion x1 (known pre-existing, verified identical with changes stashed)

[2026-10-21T13:48:02Z · bob-cli-ak.2] Recurrence marks done: new 136-recurrence-marks.js core + family dispatchers, 136/266 delegation, styles repeat glyph/ink/resting/repair flag, manifest 1.62.0, new recurrence-marks test suite 21/21 pass, date/task-tag suites 82 pass unchanged, npm build/build:check + plugin and cli docs-check green, bob plugins sync vault at 1.62.0; 6 full-suite npm failures verified identical on clean tree (pre-existing, follow-up noted)

## Dependencies

- **Depends on:** [bob-cli-ak.1](bob-cli-ak.1.md) ✓ · ⧖ 2026-10-21
- **Blocks:** [bob-cli-ak.3](bob-cli-ak.3.md) ◐ · ⧖ 2026-10-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ak.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ak.2/README.md) | [bob-cli-ak.2](bob-cli-ak.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6e34d50`](https://github.com/bobs-org/bob-cli/commit/6e34d5076b16e718a1f750fb769cba4bdc1bc5df) | docs(date-marks): specify recurrence-mark display contract and vault repeat row | [bob-cli-ak.2](bob-cli-ak.2.md) | 2026-10-21 09:50:08 EDT |
| bob-plugins | [`bob-plugins@f98f97e`](https://github.com/bobs-org/bob-plugins/commit/f98f97eeff030dcae9f66eb9e0b582631b1f9897) | feat(ledger-tools): render recurrence marks in Live Preview and rendered views | [bob-cli-ak.2](bob-cli-ak.2.md) | 2026-10-21 09:51:11 EDT |
