# Bead: bob-cli-ph.6 — One place resolver and bold drawer drafts in capture

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.6` · **Size:** large
**Created:** 2026-11-22 17:36:49 EST · **Closed:** 2026-11-25 18:24:07 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

capture-drawers: one place resolver for drawers, project sections, and notebook sections; bold draft forms in all four container contexts; `drawer_marker` spans, `**Title**` menu rows, preview drawer annotations, the `*` rewrite, catalog spelling preference, and grammar 30.

## Notes

[2026-11-25T13:38:01Z · bob-cli-ph.6] Planned remaining capture work as a five-phase child epic: shared place resolver, bold draft families, title/catalog/completion rules, editor rewrite and preview wire, then acceptance/docs. Existing bold writers are already present at 8f88a52c; no source implementation was changed in this planning turn. The child land agent must verify and close this phase only after all acceptance checks. The plan passed strict validation with zero warnings; submitting it through sase plan propose.

[2026-11-25T23:24:30Z · bob-cli-ph.6.1.land] Phase verified complete by bob-cli-ph.6.1.land; the system closed it when child epic bob-cli-ph.6.1 closed. Every item in the parent plan's capture-drawers scope is present in source and tests: place.rs one resolver for drawers/^prj sections/notebook sections; bold drafts in task, project-note, %n seed and record contexts; caps_drawer_retired and empty_drawer_bullet; drawer_marker spans and **Title** menu rows; preview drawer annotations and DrawerJson.marker; expand_drawer_marker rewrite; explicit catalog spelling preference; GRAMMAR_REVISION 30; docs. Scratch-vault walkthrough passed (bold header on @route+id, legacy NOTES append untouched, #api-design writes **API Design** from the catalog, refusal copy, capture-drawers verbatim titles). Landing fixed 3 tests broken by the epic, aligned parse with the snooze structural-key refusal, and fixed the completion-docs wording. Lib passes fully; the 17 CLI failures are the bob-cli-q4 settle-drift set, also failing at 08a708d3. epic-symbols for bob-cli-ph.6: none. See the bob-cli-ph.6.1 close note for full evidence and follow-up triage.

## Dependencies

- **Depends on:** [bob-cli-ph.4](bob-cli-ph.4.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-ph.8](bob-cli-ph.8.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-ph.9](bob-cli-ph.9.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.6.md) | [bob-cli-ph.6](bob-cli-ph.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.6.1.land][1] | Confirm the parent phase close state after the child epic closed | 2 |
| read-by | [agent:g1][2] | Check whether phase is blocked on the release gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.6.1.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.g1/README.md

<!-- sase:referenced-by:end -->
