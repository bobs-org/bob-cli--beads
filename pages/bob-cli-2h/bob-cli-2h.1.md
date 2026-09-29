# Bead: bob-cli-2h.1 — bob-cli: block-ID completion contract (intent, used IDs, suggestions, \`task\_block\_id\`)

[Bead Pages](../README.md) / [bob-cli-2h](README.md) / bob-cli-2h.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.31](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.31.md) · **Assignee:** `bob-cli-2h.1` · **Size:** medium
**Created:** 2026-09-29 09:43:07 EDT · **Closed:** 2026-09-29 10:04:49 EDT
**Plan:** [202609/mac\_block\_id\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/mac_block_id_picker.md)

## Description

bob-contract: extend `bob capture-complete` with the `task_block_id` context, the additive `block_id` object (intent, marker range, body, allowed-character rule, used IDs, suggestions), link-only candidates with Pomodoro annotations, and the project-note `+` replacement fix; update docs and tests.

## Notes

[2026-09-29T14:04:37Z · bob-cli-2h.1] PROPOSED FOLLOW-UP: clippy --all-targets fails on clean base in tests/cli/capture/pomodoro_name.rs:808 (overly_complex_bool_expr); pre-existing, unrelated to bob-contract

[2026-09-29T14:04:49Z · bob-cli-2h.1] bob-contract done: task_block_id context + block_id object (intent/marker_range/body/allowed rules/used/suggestions), link-only filtered candidates with line+pomodoro ledger annotations, + sigil excluded from replacement, suggestions per pinned examples, docs/capture.md rewritten. Verified: cargo fmt --check clean, cargo clippy --lib clean, cargo test --lib 1143 passed, cargo test --test cli capture:: 274 passed, 6 new complete_block_id integration tests pass, epic-symbols clean, real JSON outputs for link/new/project_note intents confirmed. Pre-existing clippy failure in pomodoro_name.rs:808 reproduces on base (recorded as follow-up).

## Dependencies

- **Blocks:** [bob-cli-2h.3](bob-cli-2h.3.md) ◐ · ⧖ 2026-09-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2h.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2h.1/README.md) | [bob-cli-2h.1](bob-cli-2h.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`271cadd`](https://github.com/bobs-org/bob-cli/commit/271caddeed5bf27e792c0370b854bf5703aa8023) | feat(capture): implement block-ID completion contract | [bob-cli-2h.1](bob-cli-2h.1.md) | 2026-09-29 10:06:29 EDT |
