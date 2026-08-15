# Bead: bob-cli-t.1 — Add Bob's batch grammar, protocol, and atomic transaction

[Bead Pages](../README.md) / [bob-cli-t](README.md) / bob-cli-t.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.024.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.024.w1.md) · **Assignee:** `bob-cli-t.1` · **Size:** medium
**Created:** 2026-08-15 09:47:52 EDT · **Closed:** 2026-08-15 10:15:37 EDT
**Plan:** [202608/multi\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/multi_capture.md)

## Description

bob_batch_protocol: implement shared item boundaries, cursor-aware parse and completion, additive ordered output, and all-or-nothing multi-file capture.

## Notes

[2026-08-15T14:14:52Z · bob-cli-t.1] PROPOSED FOLLOW-UP: Clean up existing clippy warnings in src/native/plugins.rs and src/native/projects.rs — cargo clippy --all-targets --all-features reports collapsible_if and question_mark suggestions unrelated to this batch-capture change.

[2026-08-15T14:15:37Z · bob-cli-t.1] Implemented shared blank-line batch grammar, item-aware parse/complete protocol, additive multi-capture JSON, staged atomic capture planning/commit with clip cleanup, docs, and tests. Verified cargo fmt --check, cargo test, cargo clippy --all-targets --all-features (exit 0; unrelated existing clippy warnings noted as proposed follow-up), and manual single/two-item capture-parse, capture-complete, and capture --dry-run --format json comparisons.

[2026-08-15T14:16:36Z · bob-cli-t.1] Verified cargo fmt --check, cargo test, cargo clippy --all-targets --all-features, git diff --check, and manual single/two-item capture-parse, capture-complete, and capture --dry-run --format json checks.

## Dependencies

- **Blocks:** [bob-cli-t.2](bob-cli-t.2.md) ✓ · ⧖ 2026-08-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-t.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-t.1/README.md) | [bob-cli-t.1](bob-cli-t.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a8c9ad8`](https://github.com/bobs-org/bob-cli/commit/a8c9ad8e8909008a64a1929e97fb831ce7339a69) | feat(capture)!: add atomic batch capture support | [bob-cli-t.1](bob-cli-t.1.md) | 2026-08-15 10:17:05 EDT |
