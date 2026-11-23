# Bead: bob-cli-on.12 — Promotion maps requirements to tasks and notes to notes

[Bead Pages](../README.md) / [bob-cli-on](README.md) / bob-cli-on.12

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.12` · **Size:** medium
**Created:** 2026-11-21 11:13:27 EST · **Closed:** 2026-11-23 01:14:26 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

## Description

promotion: rewrite nav's project seed so top-level requirements become ## Tasks rows that keep their nested requirements, notes and NOTES become ## Notes even on requirement-less tasks, and the receipt counts both.

## Notes

[2026-11-23T06:14:26Z · bob-cli-on.12] Promotion seed rewritten per §8: outer reqs become Tasks rows keeping nested reqs (NOTES filed per with_first_note), dropped/legacy/carried keep bytes, loose notes + NOTES merge into ## Notes even with no reqs, empty Tasks shows no-req notice, receipt Promoted S · t tasks · n notes wired into 667 notice. Verified: bob-plugins build + build:check clean; project-from-task 53 pass (8 new), forward-promotion 21 pass, promotion-verdicts 7 pass, project-reversal 26 pass, cycler promotion/twin suites 29 pass; bob-cli just docs-gen + docs-check pass; nav synced to vault.

## Dependencies

- **Depends on:** [bob-cli-on.11](bob-cli-on.11.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.17](bob-cli-on.17.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.12](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.12/README.md) | [bob-cli-on.12](bob-cli-on.12.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`51c31c0`](https://github.com/bobs-org/bob-cli/commit/51c31c00728c0c9c649c10af87b6c983922cc56b) | docs(projects): describe requirement promotion to tasks and notes | [bob-cli-on.12](bob-cli-on.12.md) | 2026-11-23 01:15:35 EST |
| bob-plugins | [`bob-plugins@3eb30fc`](https://github.com/bobs-org/bob-plugins/commit/3eb30fc3483e52437b1ba92b5294b554788d6eec) | feat(nav): promote requirements to tasks and notes to Notes | [bob-cli-on.12](bob-cli-on.12.md) | 2026-11-23 01:16:34 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.5x.gem][1] | Inspect remaining in-progress phases of bob-cli-on relevant to drawers and promotion | 1 |
| read-by | [agent:research.5x.grk][2] | Need promotion phase scope because drawers map to H2 on project promotion | 1 |
| read-by | [agent:research.5x.mus][3] | Drawer research: promotion conflict check | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5x.gem/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5x.grk/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5x.mus/README.md

<!-- sase:referenced-by:end -->
