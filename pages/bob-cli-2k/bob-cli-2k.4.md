# Bead: bob-cli-2k.4 — Help and docs for =x\<N\>!\<M\>

[Bead Pages](../README.md) / [bob-cli-2k](README.md) / bob-cli-2k.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.34](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.34.md) · **Assignee:** `bob-cli-2k.4` · **Size:** small
**Created:** 2026-09-29 13:45:03 EDT · **Closed:** 2026-09-29 14:44:55 EDT
**Plan:** [202609/close\_task\_selection.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/close_task_selection.md)

## Description

selection-docs: document the selection grammar, numbering, outcomes,
diagnostics, and the JSON and human output. Update `bob capture --help`,
`docs/capture.md` (grammar tables, the close section with worked examples, and
the capture-parse, capture, and capture-complete contracts), and `README.md`.

## Notes

[2026-09-29T18:44:33Z · bob-cli-2k.4] PROPOSED FOLLOW-UP: clippy deny clippy::overly_complex_bool_expr in tests/cli/capture/pomodoro_name.rs:808 (|| true) fails cargo clippy --all-targets --all-features on clean base

[2026-09-29T18:44:40Z · bob-cli-2k.4] PROPOSED FOLLOW-UP: flaky tests/gkeep_auth.rs login_missing_email_is_a_setup_error broke-pipe failure in full cargo test run, passes on retry with and without docs changes

[2026-09-29T18:44:55Z · bob-cli-2k.4] Docs done and verified: capture --help selection paragraph+examples, docs/capture.md grammar tables/new outcome subsection/parse-rewrite-complete contracts, README rows. Verified help output, parse JSON/spans/human lines (=x1,3!2,=x0,=x1,,=x!,=x 1,3,link forms) vs binary. Tests: selection 14, close 67, parse 8, capture_* 791, help 52, gkeep_auth 11 all pass; fmt clean. Pre-existing clippy deny in untouched pomodoro_name.rs recorded as follow-up.

## Dependencies

- **Depends on:** [bob-cli-2k.3](bob-cli-2k.3.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2k.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2k.4/README.md) | [bob-cli-2k.4](bob-cli-2k.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b3405bd`](https://github.com/bobs-org/bob-cli/commit/b3405bd20909d5ba1efd0e72b0c65f5c8ab88506) | docs(capture): document task-link outcome specifiers =x\[\<N\>\]\[!\<M\>\] | [bob-cli-2k.4](bob-cli-2k.4.md) | 2026-09-29 14:46:45 EDT |
