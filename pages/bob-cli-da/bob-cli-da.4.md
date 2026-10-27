# Bead: bob-cli-da.4 — Split embedded assets before the package breaches its cap

[Bead Pages](../README.md) / [bob-cli-da](README.md) / bob-cli-da.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-d7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-d7.land.md) · **Assignee:** `bob-cli-da.4` · **Size:** large
**Created:** 2026-10-27 16:30:19 EDT · **Closed:** 2026-10-27 18:40:59 EDT
**Plan:** [202610/backlog\_batch\_b2.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b2.md)

## Description

assets-split: read bob-cli-ai, if assets_split = split_now move web-clip fonts, mermaid/defuddle vendor bundles, and large assets payloads into a bob-obsidian-assets crate keeping include_bytes access, keep just package-check green with headroom, and close bob-cli-ai; if defer, record size evidence and leave the bead open with a monitor note. Do not breach the 9 MiB failure cap.

## Notes

[2026-10-27T22:41:58Z · bob-cli-da.4.1.land--1] FINAL ASSETS-SPLIT VERIFICATION: child epic bob-cli-da.4.1 is done and plan:202610/embedded_assets_split.md now has status done. The selected assets_split=split_now branch is complete: payloads are byte-identical, all 27 installed paths and executable flags are preserved, and the shared-font facade remains intact. Full just package-check verified both packages: bob-obsidian is 3,227,889 bytes (3.08 MiB; 5,160,719 bytes / 4.92 MiB under the 8 MiB warning); bob-obsidian-assets is 5,004,754 bytes (4.77 MiB; 3,383,854 bytes / 3.23 MiB under warning), versus the 8,220,034-byte pre-split root baseline. Both have substantial margin under the 9 MiB failure threshold. just check-release-tools passed 110 tests; just docs-check passed 447 tests with one font-generation dependency skip; just check-web-clip-adapter passed source and installed paths; cargo fmt --all -- --check passed. The existing just check ToolRun 4cb40f0989e9f203cd9e4c99fc4b6dfc failed two themes split catalog/completion tests tracked by bob-cli-db and outside this phase. Parent epic-symbols is clean; no just symvision recipe exists. The child close note contains the source/drift review and both follow-up outcomes. SASE closed this phase normally as delegated work landed when the child epic closed; this note records the final measurements and gate evidence. Leave bob-cli-da and bob-cli-ai open for their lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-da.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.4.md) | [bob-cli-da.4](bob-cli-da.4.md) | 0 |
