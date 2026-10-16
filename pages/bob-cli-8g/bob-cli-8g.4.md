# Bead: bob-cli-8g.4 — bob articles group with format, list, and outline

[Bead Pages](../README.md) / [bob-cli-8g](README.md) / bob-cli-8g.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1o.linker.w0.md) · **Assignee:** `bob-cli-8g.4` · **Size:** medium
**Created:** 2026-10-16 10:53:03 EDT · **Closed:** 2026-10-16 13:27:30 EDT
**Plan:** [202610/article\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/article_notes.md)

## Description

cli: register the `bob articles` Vault group (bare = list) with format (check, dry-run, stdin, json, all), list, and outline; vault discovery, preimage-checked atomic writes, colored output, completion, help, docs/articles.md, and CLI tests.

## Notes

[2026-10-16T17:19:08Z · bob-cli-8g.4--1] PROPOSED FOLLOW-UP: Clean-base just check still fails two highlights-ref note-snapshot profile tests: pandoc_maps_every_contract_construct_to_tex panics on lifted link, and renders_contract_with_clean_text_layer_and_metadata cannot render because titlesec.sty is missing. Both reproduce on clean HEAD 280321a3; neither touches the article CLI scope.

[2026-10-16T17:27:30Z · bob-cli-8g.4--2] Implemented and verified the bob articles CLI group, format/list/outline behavior, completion, docs, and integration coverage. Article unit and CLI tests passed in just check (all 2,810 library tests passed except the two pre-recorded highlights-ref profile failures reproduced on clean HEAD 280321a3); epic-symbols reported no entries.

## Dependencies

- **Depends on:** [bob-cli-8g.2](bob-cli-8g.2.md) ✓ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-8g.5](bob-cli-8g.5.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8g.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8g.4.md) | [bob-cli-8g.4](bob-cli-8g.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ff97c62`](https://github.com/bobs-org/bob-cli/commit/ff97c620d6a15f6a64c46de5e85ae29075a74afb) | feat(articles): add articles vault CLI | [bob-cli-8g.4](bob-cli-8g.4.md) | 2026-10-16 13:28:16 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8g.4--2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8g.4.md

<!-- sase:referenced-by:end -->
