# Bead: bob-cli-qm.7 — Switch the cards on, docs, approved memory, and clean deploy

[Bead Pages](../README.md) / [bob-cli-qm](README.md) / bob-cli-qm.7

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1gr](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1gr.md) · **Assignee:** `bob-cli-qm.7` · **Size:** medium
**Created:** 2026-11-26 12:38:00 EST
**Plan:** [202611/prose\_and\_notebook\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_and_notebook_cards.md)

## Description

go-live: after bob-cli-qi.6 and bob-cli-qj.4 close, delete the preview gate, extend the passive-rendering proof, finish the docs in both repos, apply the accepted memory decisions, and deploy cleanly.

## Notes

[2026-11-26T19:50:17Z · bob-cli-qp.2] COORDINATION: ref-kit (bob-cli-qp.2) owns shared-kit hunks — 240f ref species (+PROPERTY_CARD_KINDS), 240t ref predicates + precedence slot after prose, 240u ref-owned preview gate (refCardPreview), 240v shared vocabulary (refCard* before 241), 240q coordinator data-ref-source + ref kind. qm.7 gate deletion in 240t must leave these intact; ref never touches cardPreviewKinds/propertyCardKindLive. -r ref-kit coordination handoff to qm.7

[2026-11-26T21:29:16Z · bob-cli-qq.1] COORDINATION: cabinets kit adds the 240w* cabinet-owned gate/model/state/provider/collector, plus role-aware fold changes in 240s and state binding in 240r; later cabinets phases add gate-guarded hunks in 240o, 248m, and styles.css. Rendering and behavior remain current while cabinetsPreview is absent. Please keep these guarded hunks through go-live cleanup. Cabinets go-live waits for bob-cli-qm.7 and bob-cli-qp.8.

[2026-11-26T23:17:20Z · bob-cli-qm.7] PROPOSED FOLLOW-UP: Add a quiet prose provenance crumb once qj.5 defines its fields — the Prose Card can show `↰ from <owner> § <heading>` without adding provenance before the extract/inline child epic settles the contract.

## Dependencies

- **Depends on:** [bob-cli-qj.4](../bob-cli-qj/bob-cli-qj.4.md) ◐ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qm.6](bob-cli-qm.6.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qq.9](../bob-cli-qq/bob-cli-qq.9.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-qm.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qm.7.md) | [bob-cli-qm.7](bob-cli-qm.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ebc45fe`](https://github.com/bobs-org/bob-cli/commit/ebc45fece48aa486cdb59bfdbace11a3576a3ec3) | docs(cards): document Notebook and Prose cards | [bob-cli-qm.7](bob-cli-qm.7.md) | 2026-11-26 18:27:05 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qp.2][1] | Need coordination targets for ref-kit handoff | 1 |
| read-by | [agent:research.6l.cdx][2] | Verify current ownership and acceptance gates for independent ref card parallelization recommendation | 1 |
| read-by | [agent:research.6l.gem][3] | Inspect bob-cli-qi and bob-cli-qm phase details for parallel coordination and card architecture | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qp.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6l.cdx/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6l.gem/README.md

<!-- sase:referenced-by:end -->
