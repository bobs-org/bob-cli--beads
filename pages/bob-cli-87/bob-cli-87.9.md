# Bead: bob-cli-87.9 — Text-layer rule for the default Markdown profile

[Bead Pages](../README.md) / [bob-cli-87](README.md) / bob-cli-87.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10l](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10l.md) · **Assignee:** `bob-cli-87.9` · **Size:** small
**Created:** 2026-10-16 07:13:19 EDT · **Closed:** 2026-10-16 07:20:26 EDT
**Plan:** [202610/note\_snapshots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/note_snapshots.md)

## Description

markdown-text-layer: gated on default_text_layer. Make the research-report route ragged-right with no hyphenation and no common ligatures, and leave its reader and fonts as they are.

## Notes

[2026-10-16T11:20:26Z · bob-cli-87.9] Added ragged-right document settings, disabled automatic and explicit hyphenation, and disabled common ligatures via Pandoc mainfontoptions while preserving the configured fonts. Verified with cargo fmt --check, git diff --check, and cargo test --test cli highlights_create_markdown_renders_outside_xlib (1 passed); sase bead epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-87.12](bob-cli-87.12.md) ◐ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-87.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.9/README.md) | [bob-cli-87.9](bob-cli-87.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9ce50ee`](https://github.com/bobs-org/bob-cli/commit/9ce50eeb1b37f9a725850c2f4865f74afee946d7) | fix(highlights): preserve clean text layer in Markdown PDFs | [bob-cli-87.9](bob-cli-87.9.md) | 2026-10-16 07:21:05 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-87.9][1] | Need the full phase notes and design links before implementation | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-87.9/README.md

<!-- sase:referenced-by:end -->
