# Bead: bob-cli-go.8 — Split picker, section promotion, cross-note splits, and Undo notices

[Bead Pages](../README.md) / [bob-cli-go](README.md) / bob-cli-go.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.36.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.36.linker.w0.md) · **Assignee:** `bob-cli-go.8` · **Size:** medium
**Created:** 2026-11-03 16:11:31 EST · **Closed:** 2026-11-03 20:58:05 EST
**Plan:** [202611/task\_move\_merge\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_move_merge_split.md)

## Description

nav-split-picker: add the Tab-mark split picker on task lines and drawer titles, section-bullet promotion, the guarded cross-note write for daily-note owners, and a reusable Undo notice action, then document the gesture.

## Notes

[2026-11-04T01:54:13Z · bob-cli-go.8] PROPOSED FOLLOW-UP: Add required front matter to glossary:task-merge — `just docs-check` and linked bob-plugins `npm run docs:check` reproduce `memory strand has no front matter` on the clean fetched bob-cli base 751c769; parent epic bob-cli-go notes #1–3 already track this same defect, and no task bead currently matches.

[2026-11-04T01:58:05Z · bob-cli-go.8] Implemented the Tab-mark task/drawer picker, section promotion, guarded daily-note cross-note writes, cursor landing, and reusable guarded Undo notice. Verified 19 task-split tests, plugin build check, and docs inventory; synced bob-navigation-hotkeys. Docs gates pass lint but hit the pre-existing clean-base glossary:task-merge front-matter error, recorded as a proposed follow-up. No epic symbols remain.

## Dependencies

- **Depends on:** [bob-cli-go.7](bob-cli-go.7.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.9](bob-cli-go.9.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.8/README.md) | [bob-cli-go.8](bob-cli-go.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a3d44f2`](https://github.com/bobs-org/bob-cli/commit/a3d44f27e75654561673ad1ce8ac71e76a26993c) | feat(task-split): complete picker and guarded undo | [bob-cli-go.8](bob-cli-go.8.md) | 2026-11-03 21:00:29 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-go.6][1] | Need to cite the existing task tracking the docs strand front matter failure | 1 |
| read-by | [agent:bob-cli-go.8][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.6/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.8/README.md

<!-- sase:referenced-by:end -->
