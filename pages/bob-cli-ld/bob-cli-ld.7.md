# Bead: bob-cli-ld.7 — Guarded projects sync writes the catalog and retires the line

[Bead Pages](../README.md) / [bob-cli-ld](README.md) / bob-cli-ld.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c6.md) · **Assignee:** `bob-cli-ld.7` · **Size:** large
**Created:** 2026-11-13 10:58:46 EST · **Closed:** 2026-11-13 15:18:32 EST
**Plan:** [202611/subprojects\_catalog\_section.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subprojects_catalog_section.md)

## Description

catalog-sync-writer: compose lifecycle and catalog edits per file, install them through the host-catalog transaction, delete the legacy-line writer, add -f json, dry-run diffs, and a nightly step.

## Notes

[2026-11-13T19:14:58Z · bob-cli-ld.7] PROPOSED FOLLOW-UP: docs-check lint word budgets fail on a clean base for three reference files (docs/reference/json-outputs.md, docs/reference/plugins/bob-ledger-tools.md, docs/reference/plugins/bob-navigation-hotkeys.md all over the 6000-word reference cap). This implementation shortens its own json-outputs row to minimize contribution, but the gate stays red from the pre-existing overages. Evidence: timeout 300 just docs-check reports 3 lint errors on the working tree; plugin files are unmodified by this turn (git status shows no M for them) and json-outputs was already over before this turn's row. No follow-up bead created per phase instructions. -r Record pre-existing docs-check failure as follow-up per phase verification rules

[2026-11-13T19:58:44Z · bob-cli-ld.7--1] PROPOSED FOLLOW-UP: just check lib reds are pre-existing on the clean base (1501c0c3) and out of this phase's scope. Verified in a detached HEAD worktree: native::catalog::tests::public_leaves_are_entries_or_excluded (public leaf [gmail, unarchive] has no catalog entry; gmail unarchive landed in 2ddfc944 without a table row) and native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none (left [tomorrow] vs right [today, tomorrow]) fail identically without this turn's changes. Also observed one flake: native::subprocess_runner::tests::raw_run_bounds_pipe_drain_when_detached_grandchild_holds_output failed once in the full run, then passed on an unchanged-tree rerun. Full CLI suite is green (3643 passed); fmt and the full clippy gate are clean. -r Record pre-existing verification failures as follow-up per phase verification rules, no new bead per plan

[2026-11-13T20:18:32Z · bob-cli-ld.7--1] Closed by explicit `sase stitch create -B close` after create_commit landed 7cd57603 ("feat(projects)!: sync lifecycles and sub-project catalogs via host transaction"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-ld.7` if more work remains.

## Dependencies

- **Depends on:** [bob-cli-ld.3](bob-cli-ld.3.md) ✓ · ⧖ 2026-11-13
- **Depends on:** [bob-cli-ld.4](bob-cli-ld.4.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-ld.8](bob-cli-ld.8.md) ◐ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-ld.9](bob-cli-ld.9.md) ◐ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ld.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ld.7.md) | [bob-cli-ld.7](bob-cli-ld.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7cd5760`](https://github.com/bobs-org/bob-cli/commit/7cd5760320d1c05cccecb8e363918592f9aef549) | feat(projects)!: sync lifecycles and sub-project catalogs via host transaction | [bob-cli-ld.7](bob-cli-ld.7.md) | 2026-11-13 15:17:43 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ld.7--1][1] | repair failed just check gate before host completion | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ld.7.md

<!-- sase:referenced-by:end -->
