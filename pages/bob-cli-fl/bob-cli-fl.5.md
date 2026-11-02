# Bead: bob-cli-fl.5 — bob-plugins: \[off::\] writers, Obsidian start/close rule, Event marks, home chips

[Bead Pages](../README.md) / [bob-cli-fl](README.md) / bob-cli-fl.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2z.linker.w0.md) · **Assignee:** `bob-cli-fl.5` · **Size:** medium
**Created:** 2026-11-01 21:46:35 EST · **Closed:** 2026-11-02 03:20:31 EST
**Plan:** [202611/off\_clock\_pomodoros.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_clock_pomodoros.md)

## Description

plugins-off-clock-ledger: teach ledger writers [off::], apply the clock rule on se<X> starts and Ctrl+Enter closes from copied vectors, paint #offclock, and draw dashed home chips with minutes.

## Notes

[2026-11-02T08:20:05Z · bob-cli-fl.5] PROPOSED FOLLOW-UP: bob and task-status-cycler disagree on a deferred-only close — bob keeps the emptied closed row (vector close-defers-not-started-off-clock expects "- [x] (**0800-0900** [t:: 60m]) — MEET") while the plugin deletes the childless row (emptied-Pomodoro rule), so the closed headline is never stamped; decide whether the plugin should keep the row or the vector should mark it rust_only

[2026-11-02T08:20:12Z · bob-cli-fl.5] PROPOSED FOLLOW-UP: Reading-view Off-Clock detection rebuilds the row from rendered text and reconstructs Dataview inline fields from data-dv-key / .inline-field-value; it is covered by fakes only. Verify in real Obsidian that a rendered [off:: 60m] row dashes its home chip and a worked [t::] row never does (the stampedOnly guard keeps bare rows undashed in Reading view)

[2026-11-02T08:20:18Z · bob-cli-fl.5] PROPOSED FOLLOW-UP: 5 bob-plugins npm test failures reproduce identically on the clean base (not caused by this phase): test-command-mode-sheet-sequence-dom (no Chromium; tracked by bob-cli-f1), test-ledger-tools-freshness-namespace "the reload event fires only when the due key set changes", test-ledger-tools-note-ready "the startup storm is linear", test-ledger-tools-relation-index "relationIndex registers after layout-ready...", test-navigation-hotkeys-schedule-work-log "future scheduling on Pending marks Blocked but still writes the Work Log" — earlier phases recorded the same set in notes

[2026-11-02T08:20:31Z · bob-cli-fl.5] Verified in bob-plugins: [off::] key (keeps/stamps/resolves) in 020; se<X> starts follow the pomodoro_clock/meet_event_run vectors (036 counted-links rule, MEET run clock, mixed notice); task-status-cycler Ctrl+Enter restamps the closed row from kept links (062, vectors driven through completeActivePomodoroTask); #offclock/#off-clock/#untracked painted as off-clock in Live Preview + Reading; home chips dashed with minutes and 'love · 60m off the clock' tooltip, Reading view passes the flag; vectors copied byte-for-byte from bob-cli 71a65dad/8a9ec685 with README pins. npm run build:check, validate, and BOB_CLI_DIR docs:check pass; npm test has only the 5 failures that reproduce on the clean base (recorded as PROPOSED FOLLOW-UP). Versions bumped (ledger-tools 1.83.0, task-status-cycler 1.44.0); bob plugins sync deployed both (ledger-tools needed -F: the vault copy was byte-identical to committed HEAD).

## Dependencies

- **Depends on:** [bob-cli-fl.2](bob-cli-fl.2.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fl.6](bob-cli-fl.6.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.5/README.md) | [bob-cli-fl.5](bob-cli-fl.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d39b979`](https://github.com/bobs-org/bob-plugins/commit/d39b979613b0edfc7329020a6c2df8d1e82fbd1a) | feat(ledger-tools): write \[off::\] Off-Clock Pomodoros from counted Task Links | [bob-cli-fl.5](bob-cli-fl.5.md) | 2026-11-02 03:21:33 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fl.5][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.5/README.md

<!-- sase:referenced-by:end -->
