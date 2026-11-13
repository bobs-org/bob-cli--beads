# Bead: bob-cli-ld.4 — Pure sub-project catalog planner and renderer

[Bead Pages](../README.md) / [bob-cli-ld](README.md) / bob-cli-ld.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c6.md) · **Assignee:** `bob-cli-ld.4` · **Size:** medium
**Created:** 2026-11-13 10:58:46 EST · **Closed:** 2026-11-13 13:00:05 EST
**Plan:** [202611/subprojects\_catalog\_section.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subprojects_catalog_section.md)

## Description

catalog-planner: compute hosts, membership, row states, cleaned criteria, ordering, and per-host postimages (callout plus legacy-line removal) as a pure, tested planner.

## Notes

[2026-11-13T17:59:41Z · bob-cli-ld.4] PROPOSED FOLLOW-UP: just lint fails on pre-existing clippy errors in src/native/gmail/unarchive.rs (needless_borrow, useless_conversion; reproduce on clean tree)

[2026-11-13T17:59:51Z · bob-cli-ld.4] PROPOSED FOLLOW-UP: full lib suite has 4 pre-existing failures on clean tree: bank naming/import_run, native::catalog public_leaves, gcal cli sync_args; subprocess_runner pipe-drain test is flaky under full-suite load but passes in isolation

[2026-11-13T18:00:05Z · bob-cli-ld.4] Pure catalog planner landed: src/native/projects/catalog.rs (plan_catalogs/plan_host_catalog/remove_legacy_subprojects_lines/children_by_host plus criterion cleaner, ordering, and link rules) with catalog_rows::render_row. 13 new planner tests pass; cargo test --lib native::projects green (100 tests), fmt clean, clippy rustc-gate clean. just lint and 4 full-suite lib failures reproduce identically on the clean base tree (recorded as PROPOSED FOLLOW-UP); subprocess pipe-drain flake passes in isolation.

## Dependencies

- **Depends on:** [bob-cli-ld.2](bob-cli-ld.2.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-ld.6](bob-cli-ld.6.md) ✓ · ⧖ 2026-11-13
- **Blocks:** [bob-cli-ld.7](bob-cli-ld.7.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ld.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.4/README.md) | [bob-cli-ld.4](bob-cli-ld.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e8b84e3`](https://github.com/bobs-org/bob-cli/commit/e8b84e311bab32a227816e17bdd3e7fd28d7ebc0) | feat(projects)!: add pure sub-project catalog planner and renderer \[bob-cli-ld.4\] | [bob-cli-ld.4](bob-cli-ld.4.md) | 2026-11-13 13:02:17 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ld.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.4/README.md

<!-- sase:referenced-by:end -->
