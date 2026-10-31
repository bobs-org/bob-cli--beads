# Bead: bob-cli-ex.2.1.1 — Plan project task offers through the existing colon-bullet writer

[Bead Pages](../README.md) / [bob-cli-ex.2.1](bob-cli-ex.2.1.md) / bob-cli-ex.2.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ex.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ex.2.md) · **Assignee:** `bob-cli-ex.2.1.1` · **Size:** medium
**Created:** 2026-10-31 13:56:45 EDT · **Closed:** 2026-10-31 14:50:57 EDT
**Plan:** [202610/project\_note\_offer\_form.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_note_offer_form.md)

## Description

offer_engine: extend rendered project tasks, shared placement, project-note output, selection, and draft-level pull-in plumbing. Exercise ProjectNoteForm::Offer through internal planner tests while the public colon-seal grammar remains disabled.

## Notes

[2026-10-31T18:50:57Z · bob-cli-ex.2.1.1] Offer engine lands without enabling public @route:id@ grammar. Renderer returns task_rows with source identity (unnamed/hidden/closed/placeholder and TASKS-merge mapping). Planner Offer path classifies Ready/Next/Pending, freezes stable keys, applies None/All/Keys, mints selected IDs reserving authored+prj, reuses shared place_project_task_links for real links and scratch dests (probe IDs stay off the staged note). Create omits form/successors/folds. Offer JSON includes form=offer, successors with project_created, New project <basename> header, and iterator/fold/count wiring. Verified: cargo fmt --check; clippy workspace gate; 34 lib tests (capture_project_note + project_note planner + output offer tests); 245 CLI tests matching project_note/successor_offers/successor_integration/project_pull_in. epic-symbols: none.

## Dependencies

- **Blocks:** [bob-cli-ex.2.1.2](bob-cli-ex.2.1.2.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ex.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.2.1.1/README.md) | [bob-cli-ex.2.1.1](bob-cli-ex.2.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9a30ec4`](https://github.com/bobs-org/bob-cli/commit/9a30ec4ca268753820366554cd58fa5f0c006e71) | feat(capture): plan project-note task offers through the colon-bullet writer | [bob-cli-ex.2.1.1](bob-cli-ex.2.1.1.md) | 2026-10-31 14:52:17 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ex.2.1.1][1] | Need remaining notes, decisions, and whether earlier work finished | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.2.1.1/README.md

<!-- sase:referenced-by:end -->
