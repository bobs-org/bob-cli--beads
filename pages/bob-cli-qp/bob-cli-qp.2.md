# Bead: bob-cli-qp.2 — Ref species kit, preview gate, vocabulary, and scaffolding

[Bead Pages](../README.md) / [bob-cli-qp](README.md) / bob-cli-qp.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6l.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6l.linker.w0.md) · **Assignee:** `bob-cli-qp.2` · **Size:** medium
**Created:** 2026-11-26 14:22:07 EST · **Closed:** 2026-11-26 14:50:50 EST
**Plan:** [202611/ref\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ref_cards.md)

## Description

ref-kit: owns every shared-kit edit. Adds the ref species with the ribbon tile, the silent created stamp, a coordinator kind, the precedence slot after prose with the exhaustive test, a ref-owned preview gate, and one shared ref vocabulary that the Reading Board also uses. Also adds fragment stubs, fixtures, a docs stub, and coordination notes on qm.6 and qm.7.

## Notes

[2026-11-26T19:50:26Z · bob-cli-qp.2] ref-kit files: modified 240f-plugin-property-card-species.js, 240g-plugin-property-card-title-block-dom.js, 240m-plugin-property-card-created.js, 240q-plugin-property-card-frontmatter-ownership.js, 240t-plugin-property-card-note-species.js, 242-plugin-reading-board-models.js, 374-exports-property-card.js, fragments.json, styles.css, docs/nav.yml, docs/bob-ledger-tools.md, docs/index.md, package.json, plugins/bob-ledger-tools/main.js (built), manifest.json 1.168.0->1.169.0, scripts/test-ledger-tools-property-card-identity.cjs; new 240u-plugin-ref-card-preview.js, 240v-plugin-ref-card-vocabulary.js, 241a-plugin-ref-library-report-service.js, 249q/r/s/t/u/v ref-note-card stubs, 374i-exports-ref-cards.js, docs/ref-card.md, scripts/fixtures/ref-cards/ (19 notes + ref-list.json + README), scripts/test-ledger-tools-ref-note-card-kit.cjs, scripts/test-ledger-tools-ref-card-preview-gate.cjs, scripts/test-ledger-tools-ref-card-vocabulary.cjs. -r Record exact ref-kit file names per phase

[2026-11-26T19:50:43Z · bob-cli-qp.2] PROPOSED FOLLOW-UP: docs-check.sh reports pre-existing generated drift in cached bob-cli docs/develop/decisions.md (untouched by ref-kit); re-run after upstream regenerates. -r Record pre-existing docs drift

[2026-11-26T19:50:50Z · bob-cli-qp.2] ref-kit landed in bob-plugins: ref species (ribbon/bookmark/foldDefault) in 240f, icon override in 240g, silent created in 240m, data-ref-source + coordinator kind in 240q, exact-ref + library-coverage predicates and post-prose precedence in 240t, ref-owned preview gate 240u, shared vocabulary 240v with board wired byte-identical for 7 kinds, stubs 249q-v + 241a service + 374i exports, docs/ref-card.md + nav, 19 fixtures + trimmed ref-list.json, 3 new suites. Verified: npm run build + build:check green, focused ref/note-card/board suites green, full test:unit 9969 pass 0 fail 5 skipped, perf 26 pass, bob plugins sync clean (12 synced 0 drift), gate closed so no visible change. Existing registry/badge tests updated for the 12th species. COORDINATION notes left on qm.6/qm.7.

## Dependencies

- **Blocks:** [bob-cli-qp.4](bob-cli-qp.4.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qp.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qp.2/README.md) | [bob-cli-qp.2](bob-cli-qp.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b021aff`](https://github.com/bobs-org/bob-plugins/commit/b021aff56b293e8da928dca440f99ae4b99ad1d6) | feat(ledger-tools): add Ref Card kit, preview gate, vocabulary, and scaffolding | [bob-cli-qp.2](bob-cli-qp.2.md) | 2026-11-26 14:53:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qp.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qp.2/README.md

<!-- sase:referenced-by:end -->
