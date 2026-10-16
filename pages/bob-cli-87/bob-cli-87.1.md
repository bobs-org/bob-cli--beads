# Bead: bob-cli-87.1 — Bundled print fonts and glyph coverage

[Bead Pages](../README.md) / [bob-cli-87](README.md) / bob-cli-87.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10l](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10l.md) · **Assignee:** `bob-cli-87.1` · **Size:** medium
**Created:** 2026-10-16 07:13:18 EDT · **Closed:** 2026-10-16 07:35:57 EDT
**Plan:** [202610/note\_snapshots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshots.md)

## Description

fonts: vendor pinned static Source Serif 4, Inter, JetBrains Mono, and monochrome Noto Emoji faces, and expose a ttf-parser glyph-coverage API for the print profile.

## Notes

[2026-10-16T11:35:44Z · bob-cli-87.1] PROPOSED FOLLOW-UP: For bob-cli-85, evaluate replacing the web-clip variable WOFF2 fonts with these static faces to prevent Type 3 font embedding; the web-clip route stayed unchanged in this phase.

[2026-10-16T11:35:57Z · bob-cli-87.1] Vendored 13 pinned static font faces (5,976,700 font bytes); verified release SHA-256s, ttf-parser coverage for all required corpus codepoints except stripped U+FE0F, font extraction and fallback Lua output, Cargo package inclusion, targeted tests, and the full just check gate. No epic symbols remained.

## Dependencies

- **Blocks:** [bob-cli-87.4](bob-cli-87.4.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.1/README.md) | [bob-cli-87.1](bob-cli-87.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ca88db3`](https://github.com/bobs-org/bob-cli/commit/ca88db3857268fcc4a557ce9f95151d5b0e37ebf) | feat(highlights): bundle snapshot fonts and glyph coverage | [bob-cli-87.1](bob-cli-87.1.md) | 2026-10-16 07:37:00 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-87.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.1/README.md

<!-- sase:referenced-by:end -->
