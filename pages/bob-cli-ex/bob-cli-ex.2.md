# Bead: bob-cli-ex.2 — @route:id@ creates the project and offers its tasks

[Bead Pages](../README.md) / [bob-cli-ex](README.md) / bob-cli-ex.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bp.f0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bp.f0.md) · **Assignee:** `bob-cli-ex.2` · **Size:** large
**Created:** 2026-10-31 12:01:12 EDT · **Closed:** 2026-11-01 09:51:12 EST
**Plan:** [202610/project\_note\_seals.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_note_seals.md)

## Previously Closed

> ↺ Closed 2026-10-31T21:51:05Z · done
>
> delegated work landed
>
> Reopened 2026-11-01T14:04:34Z by `sase bead open`

## Description

offer_form: bob-cli adds the `@route:id@` grammar with `project_note: "offer"` spans, plus sealed `:`/`^` toggles. The project-note planner offers the new note's open tasks (never `^prj`) as successor offers in `project_note.successors`, using the existing `-p/--pull-in` and `--require-pull-in-choice` plumbing. A pick renders exactly like a ` :` bullet. Docs, glossary memory, and tests are updated.

## Notes

[2026-11-01T14:51:41Z · bob-cli-ex.2.1.land] PARENT PHASE CLOSEOUT: closed normally when its sole child epic bob-cli-ex.2.1 closed (no --force, no cascade into bob-cli-ex, which stays open for its land agent). offer_form scope verified against the working tree: @route:id@ grammar with project_note: offer spans, sealed :/^ toggles, project-note planner offers the new note's open tasks (never ^prj) as project_note.successors through the existing -p/--pull-in and --require-pull-in-choice plumbing, a pick renders byte-identically to an authored ' :' bullet, docs/glossary/tests updated. Inherited decisions honored (initial_marks=none; memory_glossary=yes for successor-offer/task-successor only, already done; no memory, option, version, or CHANGELOG changes this repair). The relaunch repair closed the two remaining gaps: route-less sealed offers (@:id@, @:id@#name, @:id@#"Lit") now refuse execution with the Pomodoro route error before any write (dry-run, submit, mixed-draft atomicity covered), and every recognized sealed offer keeps pomodoro_project_note in the editor while reporting precise route/pomodoro_id/pomodoro_name needs with byte-correct offer spans. Verification: just check ToolRun ecb03cbbbb62b69e5fb7b04c4b60c944 exit 0 (438601 ms); just docs-check passed. epic-symbols bob-cli-ex.2: none. Linked child plan plan:202610/project_note_offer_form.md status is done on plans origin/main. Declined trailing-#hide follow-up recorded on bob-cli-ex.2.1.

## Dependencies

- **Depends on:** [bob-cli-ex.1](bob-cli-ex.1.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ex.4](bob-cli-ex.4.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ex.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ex.2.md) | [bob-cli-ex.2](bob-cli-ex.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ex.2.1.1][1] | Need grandparent epic DECISIONS | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.2.1.1/README.md

<!-- sase:referenced-by:end -->
