# Bead: bob-cli-2p.1 — \`=\<X\>#pomodoro\` grammar, chains, and named session start in \`bob capture\`

[Bead Pages](../README.md) / [bob-cli-2p](README.md) / bob-cli-2p.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.36.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.36.w0.md) · **Assignee:** `bob-cli-2p.1` · **Size:** medium
**Created:** 2026-09-29 19:17:57 EDT · **Closed:** 2026-09-29 19:30:47 EDT
**Plan:** [202609/named\_pomodoro\_start.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/named_pomodoro_start.md)

## Description

execution: extend the shared `=`-family lexer with an optional `#name` part, claim `=<X>#name` (and the `=x#name` near miss) as whole-item session tokens and chain tokens, plan the named start (resolve, guard, start or create, move to the current slot, report queued links), and update JSON, human output, and `bob capture --help`.

## Notes

[2026-09-29T23:30:37Z · bob-cli-2p.1] PROPOSED FOLLOW-UP: cargo clippy --all-targets fails on untouched tests/cli/capture/pomodoro_name.rs:808 overly_complex_bool_expr (|| true); pre-existing on clean base, file untouched by this phase

[2026-09-29T23:30:47Z · bob-cli-2p.1] Implemented =<X>#name grammar, chains, named-start planner (Found/CompletedOnly-again/Missing+W1, R1/R3/R4/R5/R6), JSON/human (created) output, and capture --help. Verified: cargo fmt --check clean, cargo clippy --lib clean, cargo test all green (1238 lib + 573 cli + rest). New tests/cli/capture/pomodoro_start_named.rs covers existing/prefix/duration/again/created/W1/E1-E5/running/switch-chain/dry-run/forced.

## Dependencies

- **Blocks:** [bob-cli-2p.2](bob-cli-2p.2.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2p.4](bob-cli-2p.4.md) ✓ · ⧖ 2026-09-29
- **Blocks:** [bob-cli-2p.5](bob-cli-2p.5.md) ✓ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2p.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2p.1/README.md) | [bob-cli-2p.1](bob-cli-2p.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cba59ee`](https://github.com/bobs-org/bob-cli/commit/cba59ee919fd88f886c93735688b2994c5810b39) | feat(capture): named Pomodoro starts with =\<X\>#pomodoro | [bob-cli-2p.1](bob-cli-2p.1.md) | 2026-09-29 19:32:06 EDT |
