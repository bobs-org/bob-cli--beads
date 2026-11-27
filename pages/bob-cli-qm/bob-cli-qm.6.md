# Bead: bob-cli-qm.6 — Real-Obsidian acceptance and screenshot review for both cards

[Bead Pages](../README.md) / [bob-cli-qm](README.md) / bob-cli-qm.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1gr](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1gr.md) · **Assignee:** `bob-cli-qm.6` · **Size:** medium
**Created:** 2026-11-26 12:37:59 EST · **Closed:** 2026-11-26 17:48:47 EST
**Plan:** [202611/prose\_and\_notebook\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_and_notebook_cards.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:42891323d222e348c4b1008b | attached via sase artifact create --bead |
| related | file:explicit:a73e3835af9f399f7878ce73 | attached via sase artifact create --bead |
| related | file:explicit:cdb2d6bb57b0cc11ff575034 | attached via sase artifact create --bead |

_Plus 7 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

acceptance: after bob-cli-qi.4 closes, run both cards with the preview gate on in isolated real Obsidian across the takeover, single-owner, fail-open, data, focus, and version-skew matrix. Review the screenshot matrix and repair defects until GO.

## Notes

[2026-11-26T19:50:04Z · bob-cli-qp.2] COORDINATION: ref-kit (bob-cli-qp.2) owns shared-kit hunks — 240f ref species (+PROPERTY_CARD_KINDS), 240t ref predicates + precedence slot after prose, 240u ref-owned preview gate (refCardPreview), 240v shared vocabulary (refCard* before 241), 240q coordinator data-ref-source + ref kind. qm.7 gate deletion in 240t must leave these intact; ref never touches cardPreviewKinds/propertyCardKindLive. -r ref-kit coordination handoff to qm.6

[2026-11-26T21:29:10Z · bob-cli-qq.1] COORDINATION: cabinets kit adds the 240w* cabinet-owned gate/model/state/provider/collector, plus role-aware fold changes in 240s and state binding in 240r; later cabinets phases add gate-guarded hunks in 240o, 248m, and styles.css. Rendering and behavior remain current while cabinetsPreview is absent. Please keep these guarded hunks through go-live cleanup. Cabinets go-live waits for bob-cli-qm.7 and bob-cli-qp.8.

[2026-11-26T22:48:32Z · bob-cli-qm.6] ACCEPTANCE GO: real-Obsidian note-cards matrix 38/38 pass on bob-plugins 319862a7 + fix (bob 0.6.0 master debug build, disposable vault from shared fixtures, cardPreviewKinds set). Runner: scripts/obsidian-note-cards-e2e.cjs (sibling of the takeover runner, imports its lib, never forks it) + test wrapper registered in test:unit. Evidence: file:explicit:a73e3835af9f399f7878ce73 (report), file:explicit:cdb2d6bb57b0cc11ff575034 (run log), file:explicit:42891323d222e348c4b1008b (18-shot tar: light/dark x narrow/wide x LP/Reading x folded/expanded for both cards, album+area family, source/malformed native, forced-colors). All 18 shots + 2 grayscale conversions inspected: single card/title/foot, native hidden, H1 adopted, header absorbed, spine vs folio distinct in gray (keep initial, no pilcrow switch). REPAIRS (bob-plugins): (1) 249i double foot append — notebookCardBuildEl already appends via options.appendFoot AND notebookCardBuildMounted appended again; removed the direct call (prose had one append). (2) styles.css lint-chip white-space:nowrap — narrow-pane foot split the lint chip mid-chip. Unit: 10094/10099 pass. PROPOSED FOLLOW-UP: qj.3 commit 9426ee8f (both-spellings detection + toggle-section-numbers) never reached origin/master — Bob Prose tracks only [[article]], [[prose]] notes stay identity-only, numbering chip inert, no ready snapshot e2e possible (unit-covered; cites qm.5--1 note). PROPOSED FOLLOW-UP: test-obsidian-frontmatter-takeover-e2e screenshot-inventory expects 44, lib returns 76 after 319862a7 home-cards expansion — pre-existing on clean tree, untouched by this bead. PROPOSED FOLLOW-UP: forced-colors CDP emulation did not engage in this Electron (shots full-color); grayscale verified instead. SYNC BLOCKED: bob plugins sync refuses (ws15 uncommitted deploy @cb847f2, agent running); followed deployment doc recipe (fetch, ff to 319862a7, clean sync still refused) — no -F; qm.7 go-live owns the clean deploy after ws15 lands.

[2026-11-26T22:48:47Z · bob-cli-qm.6] GO: 38/38 real-Obsidian checks on 319862a7+fix; 20 images reviewed; double-foot + lint-wrap repaired (build+unit green); evidence in 3 bead artifacts; qj.3/qm.7 handoffs recorded as bead notes

## Dependencies

- **Depends on:** [bob-cli-qm.4](bob-cli-qm.4.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qm.5](bob-cli-qm.5.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qm.7](bob-cli-qm.7.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-qm.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qm.6/README.md) | [bob-cli-qm.6](bob-cli-qm.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@fb72a96`](https://github.com/bobs-org/bob-plugins/commit/fb72a96c6590061ac614e1a6d31f8391bfce9a42) | test(props): real-Obsidian acceptance for Notebook and Prose Cards | [bob-cli-qm.6](bob-cli-qm.6.md) | 2026-11-26 17:51:16 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qj.4][1] | Find what qm agents recorded about missing qj.3 plugin changes | 1 |
| read-by | [agent:bob-cli-qm.6][2] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-qm.7--1][3] | Collect qm.6 real-Obsidian acceptance evidence refs for qm.7 provenance note | 1 |
| read-by | [agent:bob-cli-qp.2][4] | Need coordination targets for ref-kit handoff | 1 |
| read-by | [agent:bob-cli-qp.7][5] | Learn how the sibling acceptance ran native Obsidian successfully | 2 |
| read-by | [agent:research.6l.cdx][6] | Verify current ownership and acceptance gates for independent ref card parallelization recommendation | 1 |
| read-by | [agent:research.6l.gem][7] | Inspect bob-cli-qi and bob-cli-qm phase details for parallel coordination and card architecture | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qj.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qm.6/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qm.7.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qp.2/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qp.7/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6l.cdx/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6l.gem/README.md

<!-- sase:referenced-by:end -->
