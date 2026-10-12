# Bead: bob-cli-6u.17 — Decision records, supersession marks, glossary, and docs sweep

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.17

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.17` · **Size:** small
**Created:** 2026-10-12 10:26:02 EDT · **Closed:** 2026-10-12 17:08:39 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

publish: write the project-blocking and unblocked-ticklers decision records, mark the records they partly supersede, update four glossary terms, sweep docs, and record follow-ups.

## Notes

[2026-10-12T14:45:59Z · 72] COORDINATION — In the docs sweep, keep docs/task-dependencies.md §12.10 "Project pull-in", §12.11 PP vectors (bob-cli-6t, ec7251e) and the §13.4 sentence naming §12.10. 6t.1's keep-request went to canceled 6s.13. If 6u.1 didn't port them, fix §12.10's YAML-model wording: project depends_on and frontmatter scheduled, Rule step 3 project reasons for ^prj, and PP7/PP8/PP17. Also make the recover-rank path write [unblocked::]. Add "depends_on key" and "derived field for a depends_on property" to the rg list. bob-cli-6t skipped its decision record (decision_record=no); if one is written later, it should link [[decisions/projects-block-from-prj-line]]. See research:202610/bob_cli_6t_6u_epic_conflict.md.

[2026-10-12T21:05:59Z · bob-cli-6u.17] PROPOSED FOLLOW-UP: bob-ledger-tools "blocked by project" pill for #prj_is_blocked — a ledger chip/pill that surfaces residents tagged #prj_is_blocked, listed as deliberately not doing in plan:202610/prj_line_project_blocking.md

[2026-10-12T21:06:07Z · bob-cli-6u.17] PROPOSED FOLLOW-UP: PRE-tier notice when reconcile has not run since midnight — reconcile records no last-run time today, so the walk cannot warn that unblocked fields may be stale

[2026-10-12T21:06:13Z · bob-cli-6u.17] PROPOSED FOLLOW-UP: waits on N / start-date column in bob projects list — surface ^prj open-prerequisite count and inline scheduled without a Properties/Bases view

[2026-10-12T21:06:18Z · bob-cli-6u.17] PROPOSED FOLLOW-UP: dash_projects.md projects-by-start-date query — Tasks query on #prj with scheduled after today, recovering the view frontmatter scheduled used to give

[2026-10-12T21:06:23Z · bob-cli-6u.17] PROPOSED FOLLOW-UP: retire date propagation onto residents (ADJ-8) — raise-only copies remain, including the hand-edit move-earlier limit; tag plus project_schedule would then be the only signal

[2026-10-12T21:06:28Z · bob-cli-6u.17] PROPOSED FOLLOW-UP: sub-project cascade and re-linking on unblock, if Bryan asks — both were rejected; blocking stays by residence and consumption does not restore Task Links

[2026-10-12T21:06:33Z · bob-cli-6u.17] PROPOSED FOLLOW-UP: bob-plugins date-frozen test fixtures — already recorded on bob-cli-6u.10 (19 failures also reproduce on clean base); no new bead

[2026-10-12T21:06:38Z · bob-cli-6u.17] PROPOSED FOLLOW-UP: if bob-cli-6t later writes a project-pull-in decision record (it skipped one; see bob-cli-6t.1), that record should link [[decisions/projects-block-from-prj-line]]

[2026-10-12T21:07:41Z · bob-cli-6u.17] Verified: wrote decisions/projects-block-from-prj-line and decisions/unblocked-tasks-resurface-as-ticklers; marked task-status-is-derived, task-lanes-are-sticky, ready-is-freshness-gated, rotten-keeps-use-priority-decay superseded-in-part; updated glossary task-dependency-link, project-task, task-freshness, keep-streak; sase memory init regenerated rosters (both new records + marks; glossary roster unchanged); docs sweep kept §12.10/§12.11/§13.4, recover-rank writes [unblocked::]; leftover YAML-model rg hits are hoist-only; epic-symbols empty.

[2026-10-12T21:08:39Z · bob-cli-6u.17] Verified: wrote projects-block-from-prj-line and unblocked-tasks-resurface-as-ticklers; marked task-status-is-derived, task-lanes-are-sticky, ready-is-freshness-gated, rotten-keeps-use-priority-decay superseded-in-part; updated glossary task-dependency-link, project-task, task-freshness, keep-streak; sase memory init roster shows both new records and the marks, glossary roster unchanged; docs sweep kept §12.10/§12.11/§13.4 and recover-rank writes [unblocked::]; leftover YAML-model wording is hoist-only; epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-6u.14](bob-cli-6u.14.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.15](bob-cli-6u.15.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.4](bob-cli-6u.4.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.6](bob-cli-6u.6.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.7](bob-cli-6u.7.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.9](bob-cli-6u.9.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.17](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.17.md) | [bob-cli-6u.17](bob-cli-6u.17.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |
| read-by | [agent:bob-cli-6u.8][2] | Need epic and children status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.8/README.md

<!-- sase:referenced-by:end -->
