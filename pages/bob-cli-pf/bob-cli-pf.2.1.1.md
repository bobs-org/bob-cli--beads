# Bead: bob-cli-pf.2.1.1 — Ordered frontmatter inventory and authoritative property roles

[Bead Pages](../README.md) / [bob-cli-pf.2.1](bob-cli-pf.2.1.md) / bob-cli-pf.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.md) · **Assignee:** `bob-cli-pf.2.1.1` · **Size:** medium
**Created:** 2026-11-22 14:47:18 EST · **Closed:** 2026-11-22 17:00:25 EST
**Plan:** [202611/props\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/props_cli.md)

## Description

inventory-roles: build the source-preserving props document model, semantic fingerprint, note-kind and role classifier, and show report with focused fixtures; publish the internal seams for the writer.

## Notes

[2026-11-22T22:00:25Z · bob-cli-pf.2.1.1--1] Implemented source-preserving props inventory, semantic fingerprints, note-kind and role classification, the test-only module boundary, and the shared inspect(contents, context) seam with typed diagnostics. The role code records the audited writers for derived fields and covers day/period, record, album, bank, area, project, notebook, reference, and ordinary-note contexts. Props unit tests and the full  passed (formatting, clippy, workspace tests); No --epic-symbol entries in this working tree. reported no leftovers.

[2026-11-22T22:02:18Z · bob-cli-pf.2.1.1--1] PROPOSED FOLLOW-UP: Review the timing stability of capture::related::draft_related_stays_under_the_debug_perf_gate; it passed in ToolRun 5496af44112a956d246feb1c6af32d74 and failed on the unchanged tree in ToolRun 2c1c39b14737364c1ef6c417922ecb87 at tests/cli/capture/related.rs:666.

## Dependencies

- **Blocks:** [bob-cli-pf.2.1.2](bob-cli-pf.2.1.2.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.1.1.md) | [bob-cli-pf.2.1.1](bob-cli-pf.2.1.1.md) | 0 |
