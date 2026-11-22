# Bead: bob-cli-pf.2.1.1 — Ordered frontmatter inventory and authoritative property roles

[Bead Pages](../README.md) / [bob-cli-pf.2.1](bob-cli-pf.2.1.md) / bob-cli-pf.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.md) · **Assignee:** `bob-cli-pf.2.1.1` · **Size:** medium
**Created:** 2026-11-22 14:47:18 EST · **Closed:** 2026-11-22 17:00:25 EST
**Plan:** [202611/props\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/props_cli.md)

## Description

inventory-roles: build the source-preserving props document model, semantic fingerprint, note-kind and role classifier, and show report with focused fixtures; publish the internal seams for the writer.

## Notes

[2026-11-22T22:00:25Z · bob-cli-pf.2.1.1--1] Implemented the ordered source-preserving props inventory, typed semantic fingerprint, role resolver, show report, test-only module boundary, and inspect(contents, context) seam. Documented the derived-field writer audit and covered temporal, record, album, bank, area, project, notebook, reference, and ordinary-note roles. cargo fmt, clippy, and all workspace tests passed in ToolRun 5496af44112a956d246feb1c6af32d74; the epic-symbol audit had no leftovers.

[2026-11-22T22:02:18Z · bob-cli-pf.2.1.1--1] PROPOSED FOLLOW-UP: Review the timing stability of capture::related::draft_related_stays_under_the_debug_perf_gate; it passed in ToolRun 5496af44112a956d246feb1c6af32d74 and failed on the unchanged tree in ToolRun 2c1c39b14737364c1ef6c417922ecb87 at tests/cli/capture/related.rs:666.

## Dependencies

- **Blocks:** [bob-cli-pf.2.1.2](bob-cli-pf.2.1.2.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.1.1.md) | [bob-cli-pf.2.1.1](bob-cli-pf.2.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e98c7fe`](https://github.com/bobs-org/bob-cli/commit/e98c7fe96c24e3c3b243eb05c6cd5bf4ce07b024) | feat(props): add frontmatter inventory and roles | [bob-cli-pf.2.1.1](bob-cli-pf.2.1.1.md) | 2026-11-22 17:06:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.2.1.1--1][1] | Need the assigned bead's complete current state and any prior remainder before finishing it | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.1.1.md

<!-- sase:referenced-by:end -->
