# Bead: bob-cli-56.1 — bob-ledger-tools In Progress marks

[Bead Pages](../README.md) / [bob-cli-56](README.md) / bob-cli-56.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5j](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5j.md) · **Assignee:** `bob-cli-56.1` · **Size:** medium
**Created:** 2026-10-07 10:18:28 EDT · **Closed:** 2026-10-07 10:35:07 EDT
**Plan:** [202610/in\_progress\_task\_link\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/in_progress_task_link_marks.md)

## Description

progress-marks: add a display-only half-ring mark before In Progress Task Links under today's open Pomodoros (Live Preview widget, Reading view post-processor, CSS, toggle command, refresh wiring) plus the `api.progressMarks` v1 hint namespace, with conformance tests P1-P14.

## Notes

[2026-10-07T14:35:07Z · bob-cli-56.1] progress-marks done: 137/268/269 fragments, api.progressMarks v1, toggle + refresh wiring, CSS, P1-P14 suite 22/22, full npm test 2127/2127, validate 6/6, manifest 1.34.0, README row, bob plugins sync deployed (manifest+main+styles). Deviations: 269 split for 1000-line limit; reading view maps rows via DOM ancestors (no section info in full-note views); CSS drops #c69026 (theme-safe gate forbids hex); test uses own stubs like priority-marks. Perf flake in nav stage suite passed isolated and in rerun.

## Dependencies

- **Blocks:** [bob-cli-56.4](bob-cli-56.4.md) ◐ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-56.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-56.1/README.md) | [bob-cli-56.1](bob-cli-56.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@7ea2dc8`](https://github.com/bobs-org/bob-plugins/commit/7ea2dc8e8fc20284050832cd6993d64e382af735) | feat(ledger-tools): render In Progress half-ring marks on Pomodoro Task Links (bob-cli-56.1) | [bob-cli-56.1](bob-cli-56.1.md) | 2026-10-07 10:36:55 EDT |
