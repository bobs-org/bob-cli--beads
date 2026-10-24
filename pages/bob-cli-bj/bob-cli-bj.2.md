# Bead: bob-cli-bj.2 — Shared preference journal, relation label catalog, and bob relations list/hide/unhide

[Bead Pages](../README.md) / [bob-cli-bj](README.md) / bob-cli-bj.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2e.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2e.linker.w0.md) · **Assignee:** `bob-cli-bj.2` · **Size:** medium
**Created:** 2026-10-24 13:34:45 EDT · **Closed:** 2026-10-24 15:07:01 EDT
**Plan:** [202610/relation\_label\_vocabulary.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary.md)

## Description

label-catalog: extract the theme journal into a namespaced shared module, add the relation_labels module (one key function, fast LINKS scan, display spelling, fold), the bob relations group with list/hide/unhide, the vault allowlist rollout, the label-vocabulary contract section, and shared vectors.

## Notes

[2026-10-24T19:06:43Z · bob-cli-bj.2] PROPOSED FOLLOW-UP: glossary Relation-label entry needs a glossary:relation-label memory strand plus docs-gen (docs/reference/glossary.md is generated; hand edits would drift)

[2026-10-24T19:07:01Z · bob-cli-bj.2] label-catalog landed: pref_journal shared module with themes moved onto it byte-identical (themes suites green); relation_labels key/catalog/fold/rank plus bob relations list/hide/unhide with RV7 JSON; vectors fixture consumed by 7 unit tests; 6 CLI integration tests green; live vault read-only lists 4 labels/8 links; vault allowlist committed (gitignore+gitattributes) with check-ignore/check-attr verified and vault-sync pushed; docs §16 plus CLI reference regen, docs-check green; fmt+clippy clean; full test shows only pre-existing failures (kinds themes rename old/new, 6 stable cli flakes) each reproduced identically on the clean tree via stash comparison

## Dependencies

- **Blocks:** [bob-cli-bj.3](bob-cli-bj.3.md) ◐ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bj.4](bob-cli-bj.4.md) ✓ · ⧖ 2026-10-24
- **Blocks:** [bob-cli-bj.8](bob-cli-bj.8.md) ✓ · ⧖ 2026-10-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.2/README.md) | [bob-cli-bj.2](bob-cli-bj.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`57d7761`](https://github.com/bobs-org/bob-cli/commit/57d77612109f72c1f51aecbcb43c6be106e7398b) | feat(relations): shared preference journal, label catalog, and bob relations list/hide/unhide | [bob-cli-bj.2](bob-cli-bj.2.md) | 2026-10-24 15:08:39 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bj.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.2/README.md

<!-- sase:referenced-by:end -->
