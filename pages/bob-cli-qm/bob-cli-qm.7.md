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

[2026-11-27T12:03:03Z · bob-cli-qm.7--1] PROPOSED FOLLOW-UP: three deterministic bob-navigation-hotkeys test failures on clean bob-plugins master c6fbeb36, all from the in-flight snooze work (bob-cli-q5.6.1, land agent running in ws12) — scripts/test-navigation-relation-links-stage.cjs:851 (row order now includes a new "snooze" row), scripts/test-navigation-task-card-view.cjs:2543 ("q closes from a focused More row" false!==true), and scripts/test-prose-field-roles.cjs (src/744-snooze-card-modal.js:129 text control lacks a bob-text role). Each reproduces when its file is rerun alone; none touch Prose or Notebook Card code. Full npm test: 10257 pass / 4 fail / 4 skip.

[2026-11-27T12:03:08Z · bob-cli-qm.7--1] PROPOSED FOLLOW-UP: athena /tmp tmpfs (32G) is 100% full of leftover agent acceptance fixtures (11x /tmp/bob-settings-acceptance-* at ~1G each, /tmp/bob-cli-{clean,dirty}-q5-build at 3.3G each, bob-bank-* e2e dirs), so scripts/obsidian-block-marks-e2e.cjs --self-test fails ENOSPC copying into its hardcoded /tmp/bm-e2e. Clean up the stale fixtures, and make the e2e runners honor TMPDIR and remove their scratch vaults.

[2026-11-27T12:03:13Z · bob-cli-qm.7--1] PROPOSED FOLLOW-UP (for cabinets go-live bob-cli-qq.9): scripts/obsidian-cabinets-e2e.cjs GATE_DATA and its wrapper assertion scripts/test-obsidian-cabinets-e2e.cjs:73 still seed the deleted cardPreviewKinds key ["notebook","prose"]; it is now ignored, so drop it when the cabinets gate is removed.

## Dependencies

- **Depends on:** [bob-cli-qj.4](../bob-cli-qj/bob-cli-qj.4.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qm.6](bob-cli-qm.6.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qq.9](../bob-cli-qq/bob-cli-qq.9.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-qm.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qm.7.md) | [bob-cli-qm.7](bob-cli-qm.7.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ebc45fe`](https://github.com/bobs-org/bob-cli/commit/ebc45fece48aa486cdb59bfdbace11a3576a3ec3) | docs(cards): document Notebook and Prose cards | [bob-cli-qm.7](bob-cli-qm.7.md) | 2026-11-26 18:27:05 EST |
| bob-plugins | [`bob-plugins@eca733c`](https://github.com/bobs-org/bob-plugins/commit/eca733c23a43ffad6bc2ab4bd2f7ec76eb2023ee) | feat(cards): add Notebook and Prose property cards | [bob-cli-qm.7](bob-cli-qm.7.md) | 2026-11-26 19:28:12 EST |
| bob-cli | [`eef6cc0`](https://github.com/bobs-org/bob-cli/commit/eef6cc07fe4225de1a27d052f3eee55e996b2a1a) | docs(memory): add Prose and Notebook Card glossary strands | [bob-cli-qm.7](bob-cli-qm.7.md) | 2026-11-27 07:05:01 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qj.4][1] | Find what qm agents recorded about missing qj.3 plugin changes | 1 |
| read-by | [agent:bob-cli-qm.7--1][2] | Need the phase scope, notes, and current design before resuming monitored work | 1 |
| read-by | [agent:bob-cli-qp.2][3] | Need coordination targets for ref-kit handoff | 1 |
| read-by | [agent:bob-cli-qp.8][4] | Assess qm.7 remaining work to judge ref go-live gate | 4 |
| read-by | [agent:research.6l.cdx][5] | Verify current ownership and acceptance gates for independent ref card parallelization recommendation | 1 |
| read-by | [agent:research.6l.gem][6] | Inspect bob-cli-qi and bob-cli-qm phase details for parallel coordination and card architecture | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qj.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-qm.7.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qp.2/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qp.8/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6l.cdx/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6l.gem/README.md

<!-- sase:referenced-by:end -->
