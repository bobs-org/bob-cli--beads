# Bead: bob-cli-ho.3 — Checklist stages in bob-ledger-tools (JS mirror, namespace v14, footer)

[Bead Pages](../README.md) / [bob-cli-ho](README.md) / bob-cli-ho.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.193](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.193.md) · **Assignee:** `bob-cli-ho.3` · **Size:** medium
**Created:** 2026-11-05 18:44:51 EST · **Closed:** 2026-11-05 20:39:02 EST
**Plan:** [202611/gtd\_checklist\_stages.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gtd_checklist_stages.md)

## Description

ledger_order: mirror the stage config, resolver, and comparator in the JS evaluator against a byte-for-byte copy of the shared fixture, expose stage fields under freshness namespace v14 checklistStages, and show the stage in the review footer and landing toasts.

## Notes

[2026-11-06T01:38:46Z · bob-cli-ho.3] PROPOSED FOLLOW-UP: Stabilize strict performance budgets and repair the docs link — the full plugin suite fails warm snapshot/order and keystroke-rank budgets both here and on clean base 710feae (clean base also fails cold-build; this worktree also fails the task-link viewport budget); docs-check flags the unchanged docs/task-merge.md:9 capture link.

[2026-11-06T01:39:02Z · bob-cli-ho.3] Implemented checklist-stage config, ordering, namespace v14 fields, footer and landing-toast details; added shared-fixture conformance tests and docs. Stage tests and plugin build check pass; deployed the bundle with backups. Full plugin suite retains clean-base timing-budget failures, and docs-check reaches one broken link in unchanged docs/task-merge.md:9; recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-ho.1](bob-cli-ho.1.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-ho.4](bob-cli-ho.4.md) ◐ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-ho.5](bob-cli-ho.5.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-ho.6](bob-cli-ho.6.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ho.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ho.3/README.md) | [bob-cli-ho.3](bob-cli-ho.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bac41b5`](https://github.com/bobs-org/bob-cli/commit/bac41b5baba6444f02fc2aa7946ae904a3c1ea9e) | docs(freshness): document checklist stages in JS mirror | [bob-cli-ho.3](bob-cli-ho.3.md) | 2026-11-05 20:40:23 EST |
| bob-plugins | [`bob-plugins@1017b38`](https://github.com/bobs-org/bob-plugins/commit/1017b388593966ec1482a77cd24ac6a20c3cca60) | feat(ledger-tools): mirror staged freshness checklist | [bob-cli-ho.3](bob-cli-ho.3.md) | 2026-11-05 20:40:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ho.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ho.3/README.md

<!-- sase:referenced-by:end -->
