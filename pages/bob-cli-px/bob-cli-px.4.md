# Bead: bob-cli-px.4 — Task Status Cycler closes go through the guard

[Bead Pages](../README.md) / [bob-cli-px](README.md) / bob-cli-px.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fs](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fs.md) · **Assignee:** `bob-cli-px.4` · **Size:** medium
**Created:** 2026-11-24 12:22:30 EST · **Closed:** 2026-11-24 15:29:38 EST
**Plan:** [202611/email\_task\_close\_confirmation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/email_task_close_confirmation.md)

## Description

cycler: guard Ctrl+Enter, Alt+[ / Alt+], counted, Task Link, transclusion, Pomodoro-cascade, and offer-close writes with a sync fast path, fail-closed fallback, and checkbox clicks.

## Notes

[2026-11-24T20:29:10Z · bob-cli-px.4] PROPOSED FOLLOW-UP: npm test unit flakes in scripts/test-ledger-tools-frees-marks.cjs (200-link / 2000-task 25 ms budget) and scripts/test-ledger-tools-event-link-times.cjs (200-link ledger 25 ms budget) under the full suite — isolated reruns pass; already tracked as bob-cli-io / bob-cli-km and noted on bob-cli-px.3

[2026-11-24T20:29:38Z · bob-cli-px.4] Task Status Cycler 1.59.0 guards Ctrl+Enter, Alt+[/], counted ranges, Task Links, transclusions, Pomodoro cascade, offer-close, and checkbox clicks through nav api.mailCloseGuard v1. Sync pre-check keeps non-email closes on today's path; missing nav classifies via the twin (warm cache, then vault YAML) and fails closed only when the twin says Gmail Task. Twin and vectors are byte-identical with nav. Verified: npm run build; mail-close 35 tests; pomodoro, ctrl-enter, and reference-lifecycle suites; docs:check; bob plugins sync deployed cycler 1.59.0. Full npm test: cycler tests pass; suite-load flakes in test-ledger-tools-frees-marks.cjs and test-ledger-tools-event-link-times.cjs (25 ms budgets) reproduce on clean base and are already tracked as bob-cli-io / bob-cli-km.

## Dependencies

- **Depends on:** [bob-cli-px.3](bob-cli-px.3.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-px.6](bob-cli-px.6.md) ◐ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-px.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-px.4/README.md) | [bob-cli-px.4](bob-cli-px.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6150d7e`](https://github.com/bobs-org/bob-plugins/commit/6150d7e65bd7b663ae87dc26bdbb2d9388a718eb) | feat(cycler): guard Gmail task closes with the Mail Close Card | [bob-cli-px.4](bob-cli-px.4.md) | 2026-11-24 15:30:59 EST |
