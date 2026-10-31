# Bead: bob-cli-ex.2.1 — Complete project-note task offers for bob-cli-ex.2

[Bead Pages](../README.md) / [bob-cli-ex.2](bob-cli-ex.2.md) / bob-cli-ex.2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ex.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ex.2.md) · **Assignee:** `bob-cli-ex.2.1.land`
**Created:** 2026-10-31 13:56:44 EDT · **Closed:** 2026-10-31 17:51:05 EDT
**Plan:** [202610/project\_note\_offer\_form.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_note_offer_form.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/project_note_offer_form.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_note_offer_form.md

<!-- sase:links:end -->

## Description

Capture @route:id@ creates a project note and offers its eligible tasks through the existing pull-in protocol, with selected tasks identical to authored colon bullets and complete grammar, documentation, and verification coverage.

## Notes

[2026-10-31T21:07:21Z · bob-cli-ex.2.1.land] LAND AUDIT / FOLLOW-UP TRIAGE: Reviewed all notes on bob-cli-ex.2.1.1/.2/.3, approved child/parent plans, and commits 9a30ec4c, e9b9cd1d, e8dd3b65 plus current renderer, planner, parser/rewrite, offer plumbing, acceptance tests, docs and audited glossary strands. initial_marks=none and memory_glossary=yes (only successor-offer/task-successor) honored. Fetched origin/master at e8dd3b65; drift since first child commit consists of 36c48075 (global destination removal), efe2ebe0 (Keep status) and 17702dca (Keep docs). Current parser, rewrite notices, tests and docs preserve route-only @ behavior with item-local seals; Keep changes require no project-offer integration. All child notes reviewed. Only PROPOSED FOLLOW-UP is bob-cli-ex.2.1.3 note #1: trailing #hide interpreted as a type marker. Declined the special-case grammar proposal after sase_new_task searches across bug/all types, last-week sweeps, and active-epic review: documented edge #type syntax deliberately requires escaping literal tags; installed pre-seal bob 0.4.0 reproduces type_marker_not_applicable on old @cash^pkt+ with trailing #hide, while backslash-escaped #hide and mid-text #hide parse without diagnostics. Current type_marker.rs retains that rule from pre-epic 4a95e5b7/d1dd23e2. No new task or corroboration warranted; no causal active epic issue. The installed bob predates sealed offers, so it was not used to verify the current offer implementation. Remaining epic work found by source audit: project_schedule guard is incorrectly conditioned on explicit colon tasks; final offer net pass still trusts stale line numbers for ID-less tasks and does not refresh reported final lines; its Blocked filter only checks prior Ready/Next, leaving prior Pending offers alive when later batch work blocks them. These belong to this epic and will be covered by a single medium repair tale with concrete regression cases and this epic/parent-phase closeout. Both bob-cli-ex.2.1 and bob-cli-ex.2 epic-symbol audits are empty; no symvision recipe currently exists. Epic and parent phase remain open.

[2026-10-31T21:51:05Z · bob-cli-ex.2.1.land] Landing repairs complete. Reviewed child commits 9a30ec4c (offer engine), e9b9cd1d (colon seal + protocol), e8dd3b65 (contracts + acceptance incl byte-equal Offer vs authored colon). Repaired: (1) future-project guard Offer branch in project_note.rs so s:3 Offer with only ordinary/caret-ID bullets reports link_guard project_schedule, zero offers/picks, no daily write, day-absent ok; Create unchanged; unused named-destination refusal preserved. (2) Identity reconciliation in task_complete.rs: ID-less project offers resolve by cleaned description (both sides) + frozen duplicate ordinal from offer key, not stale line; net pass refreshes final line/status after relevant mutations; later-Blocked exclusion now covers Pending '/' (Ready/Next/Pending all drop, s:0 '?' preserved byte-equal). Focused regressions in project_note_offer.rs: future-without-colon guard, line-shift stale-line, typed with fields, duplicate ordinals, selected preview/submit + partial unselected-no-ID, Pending-blocked Ready/Next/Pending. Tests: 19/19 offer pass; lib 4236 pass; full cli 2590 pass; clippy gate pass; fmt clean. Canonical sase tool run check 5dae6d51 failed once on 2 flakes (articles adopt_note_completion, complete_themes shell) that pass in isolation and in the full cli re-run; no product regression. Post-start integration: origin/master identical at e8dd3b65; non-epic 36c48075 (remove @route+id), efe2ebe0 (Keep status), 17702dca (Keep guide) preserve route-only @ + item-local seals; Keep needs no integration. Decisions honored: initial_marks none, memory_glossary yes (only successor-offer/task-successor, already complete), offers unselected, picks via colon writer no freshness, ^prj/placeholder never offered, Create unchanged, no memory edits/options, no version/CHANGELOG. Declined bob-cli-ex.2.1.3 note 1 trailing-#hide exception: documented #type grammar requires escaping literal tags; pre-seal bob reproduces refusal; \#hide and mid-text #hide pass; no duplicate/causal task; no new bead.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ex.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ex.2.1.land.md) | [bob-cli-ex.2.1](bob-cli-ex.2.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`42dd92b`](https://github.com/bobs-org/bob-cli/commit/42dd92bc66193dfc3ad16fc6ff0b9813d51c92c9) | fix(capture): finish project-offer landing repairs for bob-cli-ex.2.1 | [bob-cli-ex.2.1](bob-cli-ex.2.1.md) | 2026-10-31 17:52:51 EDT |
| bob-cli--plans | [`bob-cli--plans@4d46180`](https://github.com/bobs-org/bob-cli--plans/commit/4d461800f67260ed99d9ebd1510197189ed1875f) | docs(plans): mark project\_note\_offer\_form done for bob-cli-ex.2.1 landing | [bob-cli-ex.2.1](bob-cli-ex.2.1.md) | 2026-10-31 17:53:33 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ex.2.1.1][1] | Need parent epic DECISIONS and phase list | 1 |
| read-by | [agent:bob-cli-ex.2.1.3][2] | Need parent epic decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.2.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.2.1.3/README.md

<!-- sase:referenced-by:end -->
