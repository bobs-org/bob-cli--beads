# Bead: bob-cli-gm.1.1.4 — Activate both parsers and publish the grammar contract

[Bead Pages](../README.md) / [bob-cli-gm.1.1](bob-cli-gm.1.1.md) / bob-cli-gm.1.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-gm.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gm.1.md) · **Assignee:** `bob-cli-gm.1.1.4` · **Size:** medium
**Created:** 2026-11-03 16:48:52 EST · **Closed:** 2026-11-03 19:52:10 EST
**Plan:** [202611/capture\_target\_runs\_finish.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_target_runs_finish.md)

## Description

activate: remove internal staging, activate both resolvers together, bump the grammar once above every existing claim, document the contract, and verify CLI parity and regressions for the child epic land agent.

## Notes

[2026-11-04T00:16:58Z · bob-cli-gm.1.1.4] PROPOSED FOLLOW-UP: Repair the docs tool handling for the glossary memory strand: just docs-gen fails with “memory strand has no front matter” at sase/memory/glossary/task-merge.md, and uv run --project tools/docs bob-docs gen reproduces the identical failure on clean base 6a5b69b0; no matching task bead exists. No memory edit is authorized by the epic.

[2026-11-04T00:38:01Z · bob-cli-gm.1.1.4--1] PROPOSED FOLLOW-UP: Refresh catalog shape counts to 69 — existing task bob-cli-de tracks this stale-count defect; on clean base 6a5b69b0, native::catalog::tests::document_shape and catalog::protocol_1_parses_with_schema_version_one both fail identically with left 69/right 67.

[2026-11-04T00:52:10Z · bob-cli-gm.1.1.4--1] Completed activation with capture grammar revision 9; removed staging and corrected the remaining grammar-8 editor fixture. just check exited 101 with only native::catalog::tests::document_shape and catalog::protocol_1_parses_with_schema_version_one failing at 69 versus 67; both reproduced on clean base 6a5b69b0 and are recorded as PROPOSED FOLLOW-UP here, linked to existing task bob-cli-de. Target-run CLI tests passed for public targets and batch offsets, duplicate/split diagnostics, coded refusals, and isolated scratch-vault capture-parse/dry-run. just docs-check: bob-docs lint passed; generated drift stops at unchanged sase/memory/glossary/task-merge.md with memory strand has no front matter, reproduced on clean base and recorded on the phase. git diff --check and epic-symbol reconciliation passed.

## Dependencies

- **Depends on:** [bob-cli-gm.1.1.3](bob-cli-gm.1.1.3.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-gm.1.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gm.1.1.4.md) | [bob-cli-gm.1.1.4](bob-cli-gm.1.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c341649`](https://github.com/bobs-org/bob-cli/commit/c341649a46ad1dd58f81a0be4f3930b9315964c8) | feat(capture): activate multi-target capture runs | [bob-cli-gm.1.1.4](bob-cli-gm.1.1.4.md) | 2026-11-03 19:53:10 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gm.1.1.4--1][1] | Need final phase notes and status before closing | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-gm.1.1.4.md

<!-- sase:referenced-by:end -->
