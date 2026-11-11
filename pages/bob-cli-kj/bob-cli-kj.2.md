# Bead: bob-cli-kj.2 — Mounted reference pages back under the word cap

[Bead Pages](../README.md) / [bob-cli-kj](README.md) / bob-cli-kj.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bm](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bm.md) · **Assignee:** `bob-cli-kj.2` · **Size:** medium
**Created:** 2026-11-11 17:20:03 EST
**Plan:** [202611/impact\_ranked\_bead\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/impact_ranked_bead_fixes.md)

## Description

docs-trims: trim the four bob-mac-capture pages and one bob-plugins page that fail the 6000-word reference budget, keeping contract facts, and verify with each repo's docs gate plus bob-cli just docs-check (beads bob-cli-h9, bob-cli-jz).

## Notes

[2026-11-11T22:57:28Z · bob-cli-kj.2] Docs verification: all 5 pages trimmed to <=5800 words (protocol 6294->5787, capture-panel 6265->5785, capture-previews 6244->~5791, keyboard 6083->5644, nav-hotkeys 6200->5771; counts via bob_docs.markdown.count_words). bob-cli just docs-check: lint ok, generated drift ok. Same in mac-capture and plugins gates. Strict Zensical build still fails on 3 pre-existing link warnings in files untouched by this phase (validation.md->bob-vim-yank-flash.md#verification, keep-moving-marks.md->task-dependencies.md anchor, vault-git-sync.md->gcal.md#events); no headings added/removed, no links added except image-zoom.md, panel#inline-completion, panel#live-preview-and-clipboard-semantics, previews#close-card, protocol#timeouts-and-guards, all verified to exist.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.2.md) | [bob-cli-kj.2](bob-cli-kj.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kj.2][1] | Need phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.2.md

<!-- sase:referenced-by:end -->
