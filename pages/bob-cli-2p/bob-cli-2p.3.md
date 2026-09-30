# Bead: bob-cli-2p.3 — \`pomodoro\_start\_name\` completion context in \`bob capture-complete\`

[Bead Pages](../README.md) / [bob-cli-2p](README.md) / bob-cli-2p.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.36.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.36.w0.md) · **Assignee:** `bob-cli-2p.3` · **Size:** medium
**Created:** 2026-09-29 19:17:57 EDT · **Closed:** 2026-09-29 20:08:25 EDT
**Plan:** [202609/named\_pomodoro\_start.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/named_pomodoro_start.md)

## Description

completion: add the `pomodoro_start_name` context for the name part of `=<X>#name`, and return start-aware candidates from today's ledger: planned placeholders with `next_up`, a create row, "again" rows for completed sessions, nameable rows, and the running entry last. Include help, human output, and tests.

## Notes

[2026-09-30T00:06:57Z · bob-cli-2p.3] PROPOSED FOLLOW-UP: fix pre-existing clippy deny in untouched tests/cli/capture/pomodoro_name.rs:808 (overly_complex_bool_expr from `|| true`); `cargo clippy --all-targets --all-features` fails identically on the clean base tree

[2026-09-30T00:08:25Z · bob-cli-2p.3] pomodoro_start_name context shipped: field detection, start/again/new/name-it/running ordering with next_up, human labels, help; verified cargo test full suite green (1254 lib + 588 cli), cargo fmt clean; clippy fails only on pre-existing untouched pomodoro_name.rs:808 (recorded as follow-up)

## Dependencies

- **Depends on:** [bob-cli-2p.2](bob-cli-2p.2.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2p.4](bob-cli-2p.4.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2p.5](bob-cli-2p.5.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2p.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2p.3/README.md) | [bob-cli-2p.3](bob-cli-2p.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f41ab05`](https://github.com/bobs-org/bob-cli/commit/f41ab0550a1fe9f4ed988a3186e6d5c454f01e00) | feat(capture): add pomodoro\_start\_name completion context for =\<X\>#name | [bob-cli-2p.3](bob-cli-2p.3.md) | 2026-09-29 20:15:51 EDT |
