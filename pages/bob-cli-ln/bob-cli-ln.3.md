# Bead: bob-cli-ln.3 — bob areas list and check

[Bead Pages](../README.md) / [bob-cli-ln](README.md) / bob-cli-ln.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e2.md) · **Assignee:** `bob-cli-ln.3` · **Size:** medium
**Created:** 2026-11-14 16:33:04 EST · **Closed:** 2026-11-14 21:18:16 EST
**Plan:** [202611/areas\_catalog.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/areas_catalog.md)

## Description

areas-report: ship the read-only `bob areas` noun with list/check, the versioned JSON report (hues, project and Today rollups, catalogs, findings), a colored tree view, registration everywhere commands are listed, and the docs/areas.md contract.

## Notes

[2026-11-15T00:57:07Z · bob-cli-ln.3] PROPOSED FOLLOW-UP: docs-check lychee file-not-found for docs/bank.md link ../reference/plugins/bob-navigation-hotkeys.md#bank-walk — from the docs root that relative path builds as site/bank/index.html -> ../../reference/plugins/... (one directory too high); heading ## Bank walk exists; bank.md is unmodified this phase and the failure is independent of areas (CI does not run docs-check). No open task bead found.

[2026-11-15T02:18:16Z · bob-cli-ln.3--2] Closed by explicit `sase stitch create -B close` after create_commit landed 92813d08 ("feat(areas): add read-only bob areas list and check"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-ln.3` if more work remains.

## Dependencies

- **Depends on:** [bob-cli-ln.2](bob-cli-ln.2.md) ✓ · ⧖ 2026-11-14
- **Blocks:** [bob-cli-ln.4](bob-cli-ln.4.md) ✓ · ⧖ 2026-11-14
- **Blocks:** [bob-cli-ln.5](bob-cli-ln.5.md) ◐ · ⧖ 2026-11-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ln.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ln.3.md) | [bob-cli-ln.3](bob-cli-ln.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`92813d0`](https://github.com/bobs-org/bob-cli/commit/92813d08ea57e1f2c5cff2ae6a85e0232ed0390e) | feat(areas): add read-only bob areas list and check | [bob-cli-ln.3](bob-cli-ln.3.md) | 2026-11-14 21:17:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ln.3--2][1] | Need phase scope, notes, and close eligibility before host submit | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ln.3.md

<!-- sase:referenced-by:end -->
