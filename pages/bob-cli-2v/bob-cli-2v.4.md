# Bead: bob-cli-2v.4 — \`task\_link\` completion candidates, round-trip tests, and docs

[Bead Pages](../README.md) / [bob-cli-2v](README.md) / bob-cli-2v.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3j](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3j.md) · **Assignee:** `bob-cli-2v.4` · **Size:** medium
**Created:** 2026-09-30 13:00:14 EDT · **Closed:** 2026-09-30 13:57:48 EDT
**Plan:** [202609/task\_link\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_link_picker.md)

## Description

complete: wire discovery into the `task_link` context of `bob capture-complete`, with a pinned JSON schema, human rows, and help. Prove accept-then-capture round trips (including capture-task-id for tasks without an ID), check real-vault latency, and document the feature in docs/capture.md and README.md.

## Notes

[2026-09-30T17:57:32Z · bob-cli-2v.4] PROPOSED FOLLOW-UP: clippy logic-bug error in tests/cli/capture/pomodoro_name.rs:808 (untouched file, `|| true` at end of boolean expression) fails `cargo clippy --all-targets --all-features` on the clean base tree too; needs a fix outside this phase

[2026-09-30T17:57:48Z · bob-cli-2v.4] task_link candidates wired (pinned JSON schema, sigil-inclusive replacement, human rows, help); 6 unit + 5 CLI round-trip tests green incl. ID-less capture-task-id flow, scheduled pull-forward, 2-item batch; full cargo test green (1334 lib + 650 cli); real-vault median ~165ms at parity with ^ picker after single-pass scheduled-facts + per-note used-set optimization (target 150ms; release binary faster); docs in docs/capture.md + README; pre-existing clippy error in untouched pomodoro_name.rs recorded as follow-up

## Dependencies

- **Depends on:** [bob-cli-2v.1](bob-cli-2v.1.md) ✓ · ⧖ 2026-09-30
- **Depends on:** [bob-cli-2v.2](bob-cli-2v.2.md) ✓ · ⧖ 2026-09-30
- **Blocks:** [bob-cli-2v.5](bob-cli-2v.5.md) ◐ · ⧖ 2026-09-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2v.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2v.4/README.md) | [bob-cli-2v.4](bob-cli-2v.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b672114`](https://github.com/bobs-org/bob-cli/commit/b672114fa48247484ff4c0da0788f7a27f609d39) | feat(capture): complete task\_link picker candidates, round trips, and docs | [bob-cli-2v.4](bob-cli-2v.4.md) | 2026-09-30 14:02:04 EDT |
