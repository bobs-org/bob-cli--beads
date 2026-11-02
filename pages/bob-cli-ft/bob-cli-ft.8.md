# Bead: bob-cli-ft.8 — Cross-surface visual review, polish, and live checklist

[Bead Pages](../README.md) / [bob-cli-ft](README.md) / bob-cli-ft.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.16w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.16w.md) · **Assignee:** `bob-cli-ft.8` · **Size:** small
**Created:** 2026-11-02 06:28:11 EST · **Closed:** 2026-11-02 13:41:21 EST
**Plan:** [202611/blocked\_reason\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/blocked_reason_marks.md)

## Description

visual_review: screenshot every surface in light and dark through the e2e harness, fix polish defects against the reference mockup, run the full suites, deploy, finalize the contract's live-verification checklist, and record follow-ups.

## Notes

[2026-11-02T18:40:52Z · bob-cli-ft.8] PROPOSED FOLLOW-UP: full npm test on clean master shows 5 pre-existing failures unrelated to block marks — test-ledger-tools-freshness-namespace (reload event set), test-ledger-tools-keep-inbox (rate-limit clock text 12:30 vs 16:30), test-ledger-tools-note-ready (startup-storm linearity), test-ledger-tools-relation-index (layout-ready timing), test-navigation-hotkeys-schedule-work-log (calendar-rotted 2026-11-02 future-schedule date); all reproduce in isolation, none touch block-marks code

[2026-11-02T18:40:56Z · bob-cli-ft.8] PROPOSED FOLLOW-UP: Rust BlockReason emitting the same mark key for bob plan and the Mac Capture agenda, with a shared JSON vector fixture

[2026-11-02T18:41:03Z · bob-cli-ft.8] PROPOSED FOLLOW-UP: move task-statuses.css from a vault snippet into bob-ledger-tools so marked rows render without the snippet

[2026-11-02T18:41:21Z · bob-cli-ft.8] visual_review done: block-marks e2e passes light+dark in Live Preview and reading (top-of-note screenshots reviewed, no polish defects; digits/chevron/loop/pips centered, held vs waiting tints balanced, folds correct), task-link-marks and wikilink e2es pass with no regressions, full npm test 5139/5144 with 5 pre-existing unrelated failures recorded as follow-ups, npm run validate green, plugins docs:check green with BOB_CLI_DIR set (bare run hits a stale cache clone), just docs-check green in bob-cli; contract live-verification checklist already final, no repo changes needed so no plugins sync

## Dependencies

- **Depends on:** [bob-cli-ft.6](bob-cli-ft.6.md) ✓ · ⧖ 2026-11-02
- **Depends on:** [bob-cli-ft.7](bob-cli-ft.7.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ft.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.8/README.md) | [bob-cli-ft.8](bob-cli-ft.8.md) | 0 |
