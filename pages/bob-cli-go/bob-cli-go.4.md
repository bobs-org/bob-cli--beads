# Bead: bob-cli-go.4 — Rust merge engine for task, drawer, and section containers

[Bead Pages](../README.md) / [bob-cli-go](README.md) / bob-cli-go.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.36.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.36.linker.w0.md) · **Assignee:** `bob-cli-go.4` · **Size:** large
**Created:** 2026-11-03 16:11:30 EST · **Closed:** 2026-11-04 00:14:33 EST
**Plan:** [202611/task\_move\_merge\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_move_merge_split.md)

## Description

merge-engine: implement plan_task_merge, which validates, cuts each source's notes into the container, re-points dependents, writes the relation or Cancel Log provenance, cancels, prunes today's links, offers the target, and reports, with idempotent re-runs and property tests.

## Notes

[2026-11-03T23:11:21Z · bob-cli-go.4] PROPOSED FOLLOW-UP: Parent design research reference is missing — audited read of research:202611/task_move_merge_split_design/task_move_merge_split_design.md returned status missing on 2026-11-03; plan:202611/task_move_merge_split.md and docs/task-merge.md remain available and sufficient for the engine plan. Land agent should repair the stale citation or restore the artifact.

[2026-11-04T01:31:16Z · bob-cli-go.4.1.2] MG19 shared overlap helper (from bob-cli-go.4.1.2): task_merge::overlapping_effect_keys(path, [(list_name, [(key, name)])]) owns the one-effect-per-label rule; config/relations.rs parser now delegates its 3 lists through it with byte-identical warnings (9 relations tests green). Sibling merge-label phase: pass its 4th parsed merge_labels list through this helper, drop returned keys from ALL FOUR lists with the single warning; do NOT add RelationsConfig.merge_labels/LabelEffect::Merge/capture dispatch/CLI here. In-crate proof: mg19_shared_key_with_merge_labels_drops_everywhere_once + mg19_three_list_warnings_stay_byte_identical in src/native/task_merge/tests.rs.

[2026-11-04T05:19:17Z · bob-cli-go.4.1.land--1] Parent phase closeout evidence: bob-cli-go.4 is the parent phase of bob-cli-go.4.1 and is closed with resolution done; SASE recorded the close as “delegated work landed” when the final child epic closed, so this note supplies the requested detailed verification record. Implemented the pure `plan_task_merge(snapshot, MergeRequest, ctx)` engine for task, drawer, and section destinations; MG1-MG20 are covered, including MG19 through `task_merge::overlapping_effect_keys`. The MG19 boundary stays explicit for bob-cli-go.6: pass its fourth parsed `merge_labels` list through the helper, remove overlapping keys from all four lists with one warning, and keep public YAML/config, capture dispatch, and CLI work out of this phase. Integration preserves dependency authority, cancellation/recovery and provenance, idempotency, policy-controlled relation mirrors, successor/ledger offers, complete read-set metadata, and deterministic writes in T → dependents → other repaired notes → daily → sources order, coalescing same-note roles into one write. Verified task_merge 49/49, dependency helpers 15/15, cancellation 22/22; `sase tool run check` ecadc63fb40c41c50cd517cbf8ae2e67 passed: 4,910 library tests (2 ignored), 3,028 CLI tests, and all remaining workspace targets. `just docs-check` lint passed; its sole failure is the existing glossary strand missing front matter at `sase/memory/glossary/task-merge.md`. Integration review through HEAD 66828cfd found only adjacent capture target-run changes, with no merge/cancel/status-hook drift. Follow-ups: parent note #1's missing research artifact remains unresolved but the approved plan and `docs/task-merge.md` supplied sufficient behavior; catalog count and five task_move/task_split Clippy findings are resolved by dd90f8c7/ebedfca8; the timing flake remains tracked by bob-cli-gz and passed this full run; glossary front-matter defect remains on bob-cli-go and phase .3 notes, with no new task or memory edit. Parent epic-symbols is empty; `just symvision` is unavailable. bob-cli-go remains in progress.

## Dependencies

- **Depends on:** [bob-cli-go.1](bob-cli-go.1.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-go.2](bob-cli-go.2.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.5](bob-cli-go.5.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.6](bob-cli-go.6.md) ○ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.md) | [bob-cli-go.4](bob-cli-go.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-go.4.1.land][1] | Need parent phase acceptance and notes | 1 |
| read-by | [agent:bob-cli-go.4.1.land--1][1] | Verify the parent phase close triggered by the child and determine remaining closeout evidence | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.1.land.md

<!-- sase:referenced-by:end -->
