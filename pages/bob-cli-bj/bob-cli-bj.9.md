# Bead: bob-cli-bj.9 — Mac card rename mode

[Bead Pages](../README.md) / [bob-cli-bj](README.md) / bob-cli-bj.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2e.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2e.linker.w0.md) · **Assignee:** `bob-cli-bj.9` · **Size:** medium
**Created:** 2026-10-24 13:34:47 EDT · **Closed:** 2026-10-24 19:08:19 EDT
**Plan:** [202610/relation\_label\_vocabulary.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary.md)

## Description

mac-rename: Ctrl+R rename mode with a live dry-run preview, merge confirmation, apply on a serial long-timeout lane, the post-rename draft fix-up from bob-supplied ranges and replacements, version skew, tests, and docs.

## Notes

[2026-10-24T23:08:07Z · bob-cli-bj.9] PROPOSED FOLLOW-UP: glossary:task-relation still lacks the one-sentence relation-label vocabulary note (hide from suggestions via Ctrl+D / bob relations hide, one-off ||, global rename via bob relations rename) — this phase implements memory_glossary=no per the epic decision, so a later pass should add it once the vocabulary stabilizes

[2026-10-24T23:08:19Z · bob-cli-bj.9] mac-rename done in bob-mac-capture: Ctrl+R rename mode with live 150ms dry-run preview (relation-rename-preview lane), merge arming (first Return) + --merge apply (second Return) on the serial relation-label-pref lane with 60s timeout, post-rename draft fix-up from capture-parse label_ranges + bob replacement/hide_replacement, skew hint, Esc-first exit, docs updated. Verified: docs-check passed; full Linux swift test suite green (1648 tests, 0 failures incl. 2 new rename decode tests). macOS targets (card model/view/router/tests) could not compile here — mac unreachable — so macOS CI owns that gate.

## Dependencies

- **Blocks:** [bob-cli-bj.11](bob-cli-bj.11.md) ✓ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bj.6](bob-cli-bj.6.md) ✓ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bj.7](bob-cli-bj.7.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bj.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.9/README.md) | [bob-cli-bj.9](bob-cli-bj.9.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bj.9][1] | full read | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.9/README.md

<!-- sase:referenced-by:end -->
