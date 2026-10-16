# Bead: bob-cli-8g.5 — bob articles adopt with preview

[Bead Pages](../README.md) / [bob-cli-8g](README.md) / bob-cli-8g.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1o.linker.w0.md) · **Assignee:** `bob-cli-8g.5` · **Size:** small
**Created:** 2026-10-16 10:53:04 EDT · **Closed:** 2026-10-16 14:12:23 EDT
**Plan:** [202610/article\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/article_notes.md)

## Description

adopt: `bob articles adopt NOTE` inserts `type: "[[article]]"` plus the first format, previews by default with replaced-number reporting, writes with -w, and serves the plugin through --stdin JSON.

## Notes

[2026-10-16T17:55:50Z · bob-cli-8g.5] Implemented bob articles adopt: preview by default, -w atomic write, --stdin JSON, VaultNote completion, docs. Unit+CLI tests cover frontmatter forms, other-type/task refusals, adopt-twice noop, replaced-number preview, and stdin JSON. epic-symbols: none.

[2026-10-16T18:12:02Z · bob-cli-8g.5--1] PROPOSED FOLLOW-UP: just check --lib still fails native::highlights_ref::note_snapshot::profile tests pandoc_maps_every_contract_construct_to_tex (lifted link) and renders_contract_with_clean_text_layer_and_metadata (titlesec.sty missing on apollo). Same pair recorded on bob-cli-8g.4 against clean HEAD 280321a3; tracked by bob-cli-87. Articles adopt tests all passed (27 lib + 16 CLI).

[2026-10-16T18:12:23Z · bob-cli-8g.5--1] Implemented bob articles adopt: preview by default with replaced-number reporting, -w atomic write, --stdin JSON, VaultNote completion, docs. Unit+CLI tests passed (27 lib articles + 16 CLI articles, including frontmatter insert, other-type/task refusals, adopt-twice noop, replaced-number preview, stdin JSON). just check still fails the two pre-existing highlights-ref note-snapshot tests (titlesec.sty / lifted link) already recorded on bob-cli-8g.4 and owned by bob-cli-87. epic-symbols: none.

## Dependencies

- **Depends on:** [bob-cli-8g.4](bob-cli-8g.4.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-8g.6](bob-cli-8g.6.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8g.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8g.5.md) | [bob-cli-8g.5](bob-cli-8g.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e646cbd`](https://github.com/bobs-org/bob-cli/commit/e646cbd898f54ec99a590ce1ca9eb6ac283148f1) | feat(articles): add adopt with preview and stdin JSON | [bob-cli-8g.5](bob-cli-8g.5.md) | 2026-10-16 14:13:42 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8g.5--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8g.5.md

<!-- sase:referenced-by:end -->
