# Bead: bob-cli-3f.1 — Ready-lane-per-note contract, config, and Rust evaluator

[Bead Pages](../README.md) / [bob-cli-3f](README.md) / bob-cli-3f.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0v5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0v5.md) · **Assignee:** `bob-cli-3f.1` · **Size:** medium
**Created:** 2026-10-01 17:55:47 EDT · **Closed:** 2026-10-01 18:15:39 EDT
**Plan:** [202610/per\_note\_ready\_cap.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/per_note_ready_cap.md)

## Description

core: add plan.max_ready_per_note and the ready_cap frontmatter. Extend the area/project classifier to list forms. Build the Rust note_ready evaluator (counts, states, make-up, lints) on the freshness snapshot. Document the contract and vectors R1–R14 in docs/plan.md, and record the new decision memory.

## Notes

[2026-10-01T22:15:39Z · bob-cli-3f.1] Core done: plan.max_ready_per_note (1-999, default 5) with unit tests; classifier covers quoted/bare/flow/block-list type forms plus walk_typed_notes; new src/native/note_ready pure evaluator + scan with R1-R14 tests (17 pass); docs/plan.md Ready-cap section, lints, config; decision note-ready-cap-counts-the-lane with gated-ready superseded-in-part. Verified: cargo fmt --check clean, cargo test all green, cargo clippy exit 0.

## Dependencies

- **Blocks:** [bob-cli-3f.2](bob-cli-3f.2.md) ◐ · ⧖ 2026-10-01
- **Blocks:** [bob-cli-3f.3](bob-cli-3f.3.md) ◐ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3f.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3f.1/README.md) | [bob-cli-3f.1](bob-cli-3f.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6e04265`](https://github.com/bobs-org/bob-cli/commit/6e0426524aeed583632995fdc01ceae33f840c17) | feat(note-ready): per-note Ready cap contract, config, and Rust evaluator | [bob-cli-3f.1](bob-cli-3f.1.md) | 2026-10-01 18:17:15 EDT |
