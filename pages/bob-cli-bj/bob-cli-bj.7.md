# Bead: bob-cli-bj.7 — Mac card hide, one-off, Hidden section, and warnings

[Bead Pages](../README.md) / [bob-cli-bj](README.md) / bob-cli-bj.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2e.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2e.linker.w0.md) · **Assignee:** `bob-cli-bj.7` · **Size:** medium
**Created:** 2026-10-24 13:34:46 EDT · **Closed:** 2026-10-24 18:31:37 EDT
**Plan:** [202610/relation\_label\_vocabulary.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary.md)

## Description

mac-vocab: decode the new fields, Ctrl+D ghost-row hide/unhide on a serial lane, the one-off toggle (Ctrl+D or a typed pipe), the Hidden section and pill, the amber warning in the card, preview, and success feedback, capsule states, version skew, fixtures, and docs.

## Notes

[2026-10-24T22:31:12Z · bob-cli-bj.7] PROPOSED FOLLOW-UP: glossary:task-relation still needs its one-sentence relation-label update (hide from suggestions via Ctrl+D or bob relations hide, one-off ||, everywhere rename via bob relations rename) skipped per memory_glossary=no; records phase owns it

[2026-10-24T22:31:37Z · bob-cli-bj.7] mac-vocab done in bob-mac-capture: decode of key/inverse/hide_replacement/existing/hidden/hidden_count/one_off plus relations-list response, CaptureWarning string-or-object (fixes latent preview-decode failure on structured warnings), relation_label_hides; relation-labels and relation-label-pref lanes; Ctrl+D ghost hide/unhide with undo and background write, one-off toggle incl typed-pipe/Backspace/||-open, Ctrl+H Hidden section with pill, capsule states, amber one-off warning, context footers, amber preview row, hid notification suffix; fixtures regenerated from real bob output; docs updated. Verified: swift build --build-tests green, full portable suite 1646 tests 0 failures, swift format lint exit 0, macOS bundle.sh exit 0, typecheck-tests all PASS, docs-check passed. macOS CI run not triggered (work uncommitted); AppKit runtime tests await CI.

## Dependencies

- **Depends on:** [bob-cli-bj.1](bob-cli-bj.1.md) ✓ · ⧖ 2026-10-24
- **Depends on:** [bob-cli-bj.5](bob-cli-bj.5.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bj.9](bob-cli-bj.9.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bj.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.7/README.md) | [bob-cli-bj.7](bob-cli-bj.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@556bb67`](https://github.com/bobs-org/bob-mac-capture/commit/556bb6720136d711e81f057cee32ad21d4795c30) | feat(relation-card): hide, one-off, Hidden section, and warnings | [bob-cli-bj.7](bob-cli-bj.7.md) | 2026-10-24 18:33:16 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bj.7][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.7/README.md

<!-- sase:referenced-by:end -->
