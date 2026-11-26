# Bead: bob-cli-qp.6 — The Reference editor behind ==

[Bead Pages](../README.md) / [bob-cli-qp](README.md) / bob-cli-qp.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6l.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6l.linker.w0.md) · **Assignee:** `bob-cli-qp.6` · **Size:** medium
**Created:** 2026-11-26 14:22:08 EST · **Closed:** 2026-11-26 16:56:28 EST
**Plan:** [202611/ref\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ref_cards.md)

## Description

ref-editor: `==` opens the shared Property Editor on bob's REFERENCE contract. It has editable citation rows and owned-elsewhere rows that route reading state, residence, and file name to their owners. It probes the capability and falls back to title focus-or-add.

## Notes

[2026-11-26T21:56:06Z · bob-cli-qp.6] PROPOSED FOLLOW-UP: bob-command-mode exposes no prefill opener, so the File name row opens the sheet via its bob-command-mode:open command and copies `bob ref rename <stem> <NEW>` instead of prefilling; add an api.commandMode prefill/open-with-text entry and route the row through it.

[2026-11-26T21:56:28Z · bob-cli-qp.6] Reference editor behind == implemented and deployed. == routes on props_ref_contract_v1 (per-path cache from catalog + typed-show evidence in 298v) to settings mode on the REFERENCE contract (noteKind reference, focusSettings), else qm.1 focus-or-add on title (249v decider, 249s registration). REFERENCE contract (9 rows) in settings routing: REFERENCE SETTINGS + OWNED ELSEWHERE groups, reference-route Enter handling (reading_task opens the task or legacy notice; ref_rename opens Command Mode sheet + copies the command), title/source set-only refusals, typed stages (title/author/published/source text, aliases list, summary), = focuses settings in place, badge kind reference. bob-cli contract shape/effects already landed via qp.1. Verified: 14 new editor tests + capability/shape/route tests pass; full npm test 10084 unit + 26 perf green; build:check and docs:check green; manifest 1.170.0; bob plugins sync -p bob-ledger-tools deployed (merged origin/master incl. qp.5 readouts; package.json conflict resolved keeping both test registrations). Deviation: api.commandMode has no prefill opener, so File name always copies and best-effort opens the sheet; recorded as PROPOSED FOLLOW-UP. Memory decisions untouched (ref-go-live owns glossary:ref-card / glossary:property-card).

## Dependencies

- **Depends on:** [bob-cli-qp.1](bob-cli-qp.1.md) ✓ · ⧖ 2026-11-26
- **Depends on:** [bob-cli-qp.4](bob-cli-qp.4.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qp.7](bob-cli-qp.7.md) ◐ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qp.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qp.6/README.md) | [bob-cli-qp.6](bob-cli-qp.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f62a43e`](https://github.com/bobs-org/bob-plugins/commit/f62a43ec653018cd2536579b22b6e85a33d5e4d1) | feat(ref-card): open the Reference editor behind == | [bob-cli-qp.6](bob-cli-qp.6.md) | 2026-11-26 16:57:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qp.6][1] | check notes and remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qp.6/README.md

<!-- sase:referenced-by:end -->
