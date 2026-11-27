# Bead: bob-cli-rc.1 — Shared heading scanner and Section Map model

[Bead Pages](../README.md) / [bob-cli-rc](README.md) / bob-cli-rc.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hg](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hg.md) · **Assignee:** `bob-cli-rc.1` · **Size:** medium
**Created:** 2026-11-27 15:06:05 EST · **Closed:** 2026-11-27 15:44:41 EST
**Plan:** [202611/ctrl\_jk\_section\_map.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ctrl_jk_section_map.md)

## Description

model: refactor the section-header scanner into one walker that the keys and the map share, then add the pure Section Map model (labels, nesting depth, windowing, chips, counter, aria sentence) with unit and parity property tests.

## Notes

[2026-11-27T20:43:37Z · bob-cli-rc.1--1] PROPOSED FOLLOW-UP: Stabilize the task-link marks viewport timing guard — the full suite failed scripts/test-ledger-tools-task-link-marks-live.cjs once at 26.9ms CPU, while the clean-base focused rerun passed; this matches the intermittent report in bob-cli-f5 note #1.

[2026-11-27T20:43:46Z · bob-cli-rc.1--1] PROPOSED FOLLOW-UP: Reconcile the snooze add/resnooze history behavior with its canonical mutation vector — scripts/test-snooze-model-vectors.cjs reproduces the extra struck 1530 history row on clean HEAD, already tracked under bob-cli-q5 note #4 (corroborated by note #5).

[2026-11-27T20:44:41Z · bob-cli-rc.1--1] Implemented the shared heading walker and pure Section Map model. Build, build:check, and the focused Section Map/navigation tests (15/15) passed; diff check passed and bob plugins sync deployed the generated bundle. The full npm test gate had one intermittent timing miss that passed on clean-base rerun and the known snooze vector mismatch, reproduced on clean HEAD; both were recorded as follow-ups. No epic symbols remained.

## Dependencies

- **Blocks:** [bob-cli-rc.2](bob-cli-rc.2.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-rc.3](bob-cli-rc.3.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rc.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-rc.1.md) | [bob-cli-rc.1](bob-cli-rc.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@44425a4`](https://github.com/bobs-org/bob-plugins/commit/44425a4929a93d170b1ed0845d7ded3b5ef9adf3) | feat(navigation): add shared Section Map model | [bob-cli-rc.1](bob-cli-rc.1.md) | 2026-11-27 15:24:25 EST |
| bob-plugins | [`bob-plugins@d4edb02`](https://github.com/bobs-org/bob-plugins/commit/d4edb022697087d994ded538800a77a00063af2a) | fix(navigation): refresh the Section Map bundle for single-heading notes | [bob-cli-rc.1](bob-cli-rc.1.md) | 2026-11-27 15:45:38 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-rc.1--1][1] | Verify the two required follow-up notes before final closeout | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-rc.1.md

<!-- sase:referenced-by:end -->
