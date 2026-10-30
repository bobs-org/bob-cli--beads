# Bead: bob-cli-e6.12 — bob ref today and successor offers place by type

[Bead Pages](../README.md) / [bob-cli-e6](README.md) / bob-cli-e6.12

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2t.linker.w0.md) · **Assignee:** `bob-cli-e6.12` · **Size:** medium
**Created:** 2026-10-29 16:16:34 EDT · **Closed:** 2026-10-30 00:18:09 EDT
**Plan:** [202610/task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_types.md)

## Description

ref-today-successors: place reading-task links and successor links by their own type in Rust and task-status-cycler, and retype on explicit ref-today targets.

## Notes

[2026-10-30T04:03:15Z · bob-cli-e6.12] PROPOSED FOLLOW-UP: Reconcile generated-doc drift in docs/reference/glossary.md and docs/develop/decisions.md; bob-plugins docs:check fails identically on the clean bob-cli base. bob-cli-ea.3 #2 already recorded the same gate failure, and bob-cli-ar tracks a related Successor Offer glossary source defect; lander should consolidate rather than file duplicate work.

[2026-10-30T04:18:09Z · bob-cli-e6.12] Implemented typed default placement for bob ref today and Rust/task-status-cycler successor offers, plus explicit ref-today retyping; updated docs and deployed task-status-cycler. Verified cargo fmt --check, cargo check --bin bob, 41 Rust successor tests, 4 focused ref-today tests, 17 plugin successor tests, npm run build, and npm run build:check. bob-plugins docs:check lint passes but generated drift in docs/reference/glossary.md and docs/develop/decisions.md reproduces on clean base; recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Blocks:** [bob-cli-e6.16](bob-cli-e6.16.md) ◐ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.7](bob-cli-e6.7.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.8](bob-cli-e6.8.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e6.12](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.12/README.md) | [bob-cli-e6.12](bob-cli-e6.12.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`175b749`](https://github.com/bobs-org/bob-cli/commit/175b7498a1471308de85f9736284ee97477d0358) | feat(ref)!: bob ref today places reading tasks by type | [bob-cli-e6.12](bob-cli-e6.12.md) | 2026-10-30 00:19:18 EDT |
| bob-plugins | [`bob-plugins@6562b63`](https://github.com/bobs-org/bob-plugins/commit/6562b63522c8c1d333c2f3c426db7e005cb0a592) | feat(task-status-cycler): successor offers place by task type | [bob-cli-e6.12](bob-cli-e6.12.md) | 2026-10-30 00:21:38 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e6.12][1] | Final review before phase closeout | 2 |
| read-by | [agent:bob-cli-e6.7][2] | Confirm e6.12 owns ref-today typed placement to route the parity seam | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.12/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.7/README.md

<!-- sase:referenced-by:end -->
