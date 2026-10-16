# Bead: bob-cli-8g.1 — Pure article formatter core

[Bead Pages](../README.md) / [bob-cli-8g](README.md) / bob-cli-8g.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1o.linker.w0.md) · **Assignee:** `bob-cli-8g.1` · **Size:** medium
**Created:** 2026-10-16 10:53:03 EDT · **Closed:** 2026-10-16 11:49:46 EDT
**Plan:** [202610/article\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/article_notes.md)

## Description

engine: bob-cli src/native/articles/ pure core: article marker and refusals, block scanner, section levels and numbering with the ownership token, layout rules, word invariant, idempotency, golden fixtures, and a read-only vault corpus test.

## Notes

[2026-10-16T15:49:20Z · bob-cli-8g.1] PROPOSED FOLLOW-UP: capture-templates kinds and NativeCommand coverage — reproduces identically on clean master: every_value_arg_has_a_decision missing capture-templates delete:template, save:template-origin, show:template; every_native_command_is_on_exactly_one_canonical_path 36 vs 31. Already on bob-cli-8b note #1 and bob-cli-8f.1.

[2026-10-16T15:49:27Z · bob-cli-8g.1] PROPOSED FOLLOW-UP: note_snapshot titlesec.sty missing — renders_contract_with_clean_text_layer_and_metadata fails identically on clean master: xelatex pass 1 cannot find titlesec.sty. Environment gap; already recorded on bob-cli-8f.1.

[2026-10-16T15:49:46Z · bob-cli-8g.1] Verified pure article formatter core: src/native/articles/ (marker, scan, sections, layout, verify, plan) plus generalized type matcher frontmatter_is_article. cargo test --lib articles: 15 passed, 1 ignored. BOB_ARTICLES_CORPUS=$HOME/bob corpus_no_panic: zero words-changed/not-idempotent failures. cargo fmt --check and clippy rustc_gate green. just check: fmt+clippy green; lib 2748 passed, 3 failed identically on clean master (capture-templates kinds + NativeCommand 36 vs 31 on bob-cli-8b; titlesec.sty missing on bob-cli-8f.1). No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-8g.2](bob-cli-8g.2.md) ◐ · ⧖ 2026-10-16
- **Blocks:** [bob-cli-8g.3](bob-cli-8g.3.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8g.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8g.1/README.md) | [bob-cli-8g.1](bob-cli-8g.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8e96375`](https://github.com/bobs-org/bob-cli/commit/8e9637538ecee897cb0bbc5809c0e056cf311d7f) | feat(articles): add pure article formatter core | [bob-cli-8g.1](bob-cli-8g.1.md) | 2026-10-16 12:04:49 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8g.1][1] | Need the phase scope and design file for number-replaced finding contract | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8g.1/README.md

<!-- sase:referenced-by:end -->
