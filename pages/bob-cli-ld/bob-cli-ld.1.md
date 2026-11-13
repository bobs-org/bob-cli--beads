# Bead: bob-cli-ld.1 — PROJECTS region spec and generated-heading guards

[Bead Pages](../README.md) / [bob-cli-ld](README.md) / bob-cli-ld.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c6.md) · **Assignee:** `bob-cli-ld.1` · **Size:** small
**Created:** 2026-11-13 10:58:46 EST · **Closed:** 2026-11-13 11:26:29 EST
**Plan:** [202611/subprojects\_catalog\_section.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subprojects_catalog_section.md)

## Description

catalog-guards: add the PROJECTS RegionSpec and make every generated catalog heading (Notebooks, Albums, Projects) a never-drawer, never-section-target heading, fixing the live #notebooks drawer bug.

## Notes

[2026-11-13T16:26:04Z · bob-cli-ld.1] PROPOSED FOLLOW-UP: repair clean-base gates — `just check` reproduces five Clippy errors in untouched src/native/gmail/unarchive.rs; `just docs-check` reproduces json-outputs.md (6008/6000), plugins/bob-ledger-tools.md (6136/6000), and plugins/bob-navigation-hotkeys.md (6055/6000). No exact follow-up task found for the Gmail or Ledger Tools failures; navigation budget is tracked by bob-cli-jz, and json-outputs previously crossed the cap in bob-cli-k3.2.1 (now closed).

[2026-11-13T16:26:29Z · bob-cli-ld.1] Implemented PROJECTS RegionSpec and shared generated-catalog heading guards for capture, section targets, and merges. Verified capture placement/drawer and merge tests, cargo fmt, and git diff --check; clean-base just check and docs-check failures recorded in PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-ld.2](bob-cli-ld.2.md) ✓ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ld.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.1/README.md) | [bob-cli-ld.1](bob-cli-ld.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2709046`](https://github.com/bobs-org/bob-cli/commit/2709046a2a7912fc19f741e085bfd4e406a2d541) | feat(capture): protect generated project catalog heading | [bob-cli-ld.1](bob-cli-ld.1.md) | 2026-11-13 11:28:53 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ld.1][1] | Confirm the assigned phase is closed after implementation and verification | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ld.1/README.md

<!-- sase:referenced-by:end -->
