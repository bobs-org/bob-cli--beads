# Bead: bob-cli-qm.4 — Notebook Card report-backed readouts

[Bead Pages](../README.md) / [bob-cli-qm](README.md) / bob-cli-qm.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1gr](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1gr.md) · **Assignee:** `bob-cli-qm.4` · **Size:** medium
**Created:** 2026-11-26 12:37:59 EST · **Closed:** 2026-11-26 14:37:26 EST
**Plan:** [202611/prose\_and\_notebook\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_and_notebook_cards.md)

## Description

notebook-readouts: add the note count, newest date, section chips that jump to their headings, child notebooks, an error pill, and lint from the existing shared notebook report, with zero new spawns and no layout shift.

## Notes

[2026-11-26T19:37:13Z · bob-cli-qm.4] PROPOSED FOLLOW-UP: docs/develop/decisions.md generated drift fails npm run docs:check identically on the clean tree (verified via stash); see bob-cli-qm.2 note #1 which already tracks this pre-existing drift — re-triage there instead of fixing here.

[2026-11-26T19:37:26Z · bob-cli-qm.4] notebook-readouts done and verified on rebased origin/master (3863bc4 + this work). 249k readouts: one plugin-level apiNotebookSubscribe patches mounted cards in place and releases on unload; readout line (N notes, newest authored date, folded section count), section chips with order/title-fallback pairing, inert stale chips, 7+ +N session overflow, child chips, error pill with line jump, warnings into foot lint; nothing paints without a fresh row, never zeroes. Host (249i) + foot (249j) + mixin registration + styles + 374h exports + docs/notebook-card.md + manifest 1.169.0 + docs regen. Verified: npm run build, build:check, docs:inventory:check, focused 106 pass, full npm test 9969 unit + 26 perf with 0 fail (incl. new readouts suite with no-spawn spy), bob plugins sync clean after ff-merge of landed prose bundle + rebuild (3 copied). Real-app/acceptance evidence stays with bob-cli-qm.6. Pre-existing npm run docs:check decisions.md drift reproduces on clean tree (see qm.2 note #1; follow-up noted).

## Dependencies

- **Depends on:** [bob-cli-qm.2](bob-cli-qm.2.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qm.6](bob-cli-qm.6.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-qm.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qm.4/README.md) | [bob-cli-qm.4](bob-cli-qm.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f6458cb`](https://github.com/bobs-org/bob-plugins/commit/f6458cb04930d45ce340e91828ce2dd52a23ba45) | feat(ledger-tools): add Notebook Card report-backed readouts | [bob-cli-qm.4](bob-cli-qm.4.md) | 2026-11-26 14:38:22 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.6l.gem][1] | Inspect bob-cli-qi and bob-cli-qm phase details for parallel coordination and card architecture | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.6l.gem/README.md

<!-- sase:referenced-by:end -->
