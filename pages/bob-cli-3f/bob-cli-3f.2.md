# Bead: bob-cli-3f.2 — bob ready command

[Bead Pages](../README.md) / [bob-cli-3f](README.md) / bob-cli-3f.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0v5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0v5.md) · **Assignee:** `bob-cli-3f.2` · **Size:** medium
**Created:** 2026-10-01 17:55:47 EDT · **Closed:** 2026-10-01 18:46:05 EDT
**Plan:** [202610/per\_note\_ready\_cap.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/per_note_ready_cap.md)

## Description

cli: add the read-only top-level `bob ready [NOTE]`: a colored CROWDED/FULL/ROOM bar view, a per-note worklist, schema-1 JSON, --check (exit 3), --cap preview, and --all. Includes help, README, justfile smoke, and integration tests.

## Notes

[2026-10-01T22:46:05Z · bob-cli-3f.2] bob ready ships: overview/worklist/human+JSON/--check/--cap/--all with 19 integration tests + 5 render unit tests. Verified: cargo fmt --check clean, clippy clean for touched files (1 pre-existing TypedNote warning untouched), full cargo test green (1461 lib + 718 cli), live-vault wall time ready-overview ~7.0s vs freshness list ~7.8s (worklist-only lane passes skipped in overview). epic-symbols: none.

## Dependencies

- **Depends on:** [bob-cli-3f.1](bob-cli-3f.1.md) ✓ · ⧖ 2026-10-01
- **Blocks:** [bob-cli-3f.5](bob-cli-3f.5.md) ◐ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3f.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3f.2/README.md) | [bob-cli-3f.2](bob-cli-3f.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`812c1b1`](https://github.com/bobs-org/bob-cli/commit/812c1b19ac8402dd92c6fd451405e6a853341c97) | feat(ready): add bob ready per-note Ready-cap view | [bob-cli-3f.2](bob-cli-3f.2.md) | 2026-10-01 18:48:02 EDT |
