# Bead: bob-cli-8g.6 — Inbound heading links, nightly check, and memory

[Bead Pages](../README.md) / [bob-cli-8g](README.md) / bob-cli-8g.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1o.linker.w0.md) · **Assignee:** `bob-cli-8g.6` · **Size:** medium
**Created:** 2026-10-16 10:53:04 EDT · **Closed:** 2026-10-16 15:09:19 EDT
**Plan:** [202610/article\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/article_notes.md)

## Description

inbound: rewrite links from other notes when an article's headings change (CLI writes, plugin plans), report unrepairable ones, add a report-only nightly step, and apply any accepted memory decisions.

## Notes

[2026-10-16T19:09:11Z · bob-cli-8g.6] PROPOSED FOLLOW-UP: lib tests native::highlights_ref::note_snapshot::profile::tests::pandoc_maps_every_contract_construct_to_tex (panic: lifted link) and renders_contract_with_clean_text_layer_and_metadata (xelatex missing titlesec.sty) fail identically on clean HEAD; already tracked by bob-cli-87.

[2026-10-16T19:09:19Z · bob-cli-8g.6] Inbound heading-link repair rewrites two other notes (wikilink + markdown percent-encoding), reports unrepairable/ambiguous inbound-heading-link findings with path:line, skips drifted preimages, fills stdin JSON inbound, and shows dry-run inbound diffs. Nightly adds a report-only articles step after task archive that prints needs-formatting and still passes. Memory strands skipped per approved decisions (memory_glossary=no, memory_decision=no). Verified: inbound unit tests, articles CLI inbound tests, nightly CLI tests, help goldens; just check fmt/clippy/CLI green. Two highlights_ref snapshot tests fail identically on clean HEAD (bob-cli-87). No --epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-8g.5](bob-cli-8g.5.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-8g.7](bob-cli-8g.7.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-8g.8](bob-cli-8g.8.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8g.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8g.6/README.md) | [bob-cli-8g.6](bob-cli-8g.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`93a76ed`](https://github.com/bobs-org/bob-cli/commit/93a76ed3876b4a9221ad258def1cca3ed450e321) | feat(articles): repair inbound heading links and add nightly check | [bob-cli-8g.6](bob-cli-8g.6.md) | 2026-10-16 15:10:35 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8g.6][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8g.6/README.md

<!-- sase:referenced-by:end -->
