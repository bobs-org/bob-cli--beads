# Bead: bob-cli-ln.1 — Shared catalog engine - AREAS spec, placement order, heading adoption, capture guard

[Bead Pages](../README.md) / [bob-cli-ln](README.md) / bob-cli-ln.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e2.md) · **Assignee:** `bob-cli-ln.1` · **Size:** medium
**Created:** 2026-11-14 16:33:03 EST · **Closed:** 2026-11-14 17:12:36 EST
**Plan:** [202611/areas\_catalog.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/areas_catalog.md)

## Description

catalog-engine: add the AREAS region spec and the AfterSectionThenFirstH2 placement, move PROJECTS below an existing Areas section, teach every catalog to adopt an authored heading instead of duplicating it, and refuse capture into `## Areas`.

## Notes

[2026-11-14T22:12:36Z · bob-cli-ln.1] catalog-engine done: AREAS spec first in GENERATED_CATALOGS, PROJECTS AfterSectionThenFirstH2(Areas), heading adoption for all families, areas_section_generated guard. Verified: 25 host_catalog::region tests, 147 host_catalog+notebooks+projects+placement tests, full native::capture suite (2032 passed), cargo fmt --check and clippy clean. No existing duplicate-heading tests needed updates.

## Dependencies

- **Blocks:** [bob-cli-ln.2](bob-cli-ln.2.md) ◐ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ln.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ln.1/README.md) | [bob-cli-ln.1](bob-cli-ln.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`13fdf78`](https://github.com/bobs-org/bob-cli/commit/13fdf78d201c696cb0501c1b6b60c45246db1b45) | feat(areas): shared catalog engine for generated Areas catalogs | [bob-cli-ln.1](bob-cli-ln.1.md) | 2026-11-14 17:15:25 EST |
