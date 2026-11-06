# Bead: bob-cli-ho.4 — Stage labels beside the sunrise and flag in the editor

[Bead Pages](../README.md) / [bob-cli-ho](README.md) / bob-cli-ho.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.193](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.193.md) · **Assignee:** `bob-cli-ho.4` · **Size:** medium
**Created:** 2026-11-05 18:44:51 EST · **Closed:** 2026-11-05 21:02:46 EST
**Plan:** [202611/gtd\_checklist\_stages.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gtd_checklist_stages.md)

## Description

stage_labels: specify and render a quiet small-caps stage label right after the PRE sunrise / POST flag in Live Preview and Reading view, only for a configured stage tag adjacent to the identity run, with tooltip, reveal, toggle, and light/dark checks.

## Notes

[2026-11-06T02:02:27Z · bob-cli-ho.4] PROPOSED FOLLOW-UP: docs-check lychee flags one broken link (task-merge page to docs/capture#merging-tasks-into-a-new-task-with); reproduces identically on the clean base tree in both bob-cli (just docs-check) and bob-plugins (npm run docs:check), so unrelated to stage_labels

[2026-11-06T02:02:46Z · bob-cli-ho.4] Stage labels implemented: contract SL1-SL12 in docs/task-tag-marks.md; core + Live Preview/Reading view in bob-ledger-tools (138/264/264a/350/310/fragments); styles; manifest 1.101.0. Verified: full npm test 5605 pass, focused task-tag/freshness 83 pass, build:check + inventory pass, bob plugins sync deployed ledger-tools. docs-check lychee failure is pre-existing on clean tree (noted as follow-up). Changes uncommitted in working trees for stitch.

## Dependencies

- **Depends on:** [bob-cli-ho.3](bob-cli-ho.3.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-ho.6](bob-cli-ho.6.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ho.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ho.4/README.md) | [bob-cli-ho.4](bob-cli-ho.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6ea08f7`](https://github.com/bobs-org/bob-cli/commit/6ea08f74c0ba08e5c313ea8f9cce6e40edb109c4) | docs(marks): add checklist stage labels contract (SL1-SL12) | [bob-cli-ho.4](bob-cli-ho.4.md) | 2026-11-05 21:04:18 EST |
