# Bead: bob-cli-cc.2 — Render-time code catalog on both pandoc routes

[Bead Pages](../README.md) / [bob-cli-cc](README.md) / bob-cli-cc.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5b.linker.w0.md) · **Assignee:** `bob-cli-cc.2` · **Size:** medium
**Created:** 2026-10-26 09:00:55 EDT · **Closed:** 2026-10-26 10:32:04 EDT
**Plan:** [202610/ref\_code\_block\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_code_block_copy.md)

## Description

catalog: add the two-pass code-catalog Lua filter, invisible per-block PDF anchors, --preserve-tabs with filter-side tab expansion, the frozen render input, and the promoted /Dests reader, so every Markdown and snapshot render returns an exact CodeCatalog with pages while the PDF stays unchanged.

## Notes

[2026-10-26T14:32:04Z · bob-cli-cc.2--4] Verified the targeted snapshot profile tests, just docs-check, and full just check pass after updating the generic-route filter assertion to code-break.lua. sase bead epic-symbols bob-cli-cc.2 reported no remaining entries.

## Dependencies

- **Blocks:** [bob-cli-cc.3](bob-cli-cc.3.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cc.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-cc.2.md) | [bob-cli-cc.2](bob-cli-cc.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c7ced49`](https://github.com/bobs-org/bob-cli/commit/c7ced497d875f5c569d1a324ca9ac5a59a6e49eb) | feat(highlights-ref): build render-time code catalog | [bob-cli-cc.2](bob-cli-cc.2.md) | 2026-10-26 10:32:44 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-cc.2--4][1] | Confirm the assigned phase closed before final declaration | 2 |
| read-by | [agent:bob-cli-cc.3][2] | Check prior phases landed | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-cc.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.3/README.md

<!-- sase:referenced-by:end -->
