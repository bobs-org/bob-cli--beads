# Bead: bob-cli-a2.11 — Task Card \`l\` Links to… and the Links stage with the relation field

[Bead Pages](../README.md) / [bob-cli-a2](README.md) / bob-cli-a2.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.53.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.53.linker.w0.md) · **Assignee:** `bob-cli-a2.11` · **Size:** medium
**Created:** 2026-10-20 09:08:23 EDT · **Closed:** 2026-10-20 11:35:41 EDT
**Plan:** [202610/task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_relations.md)

## Description

nav-links-stage: add the Task Card row `l` and Ctrl+Shift+L, the Links stage (open, closed, then archived pool; CURRENT, RESULTS, and CLOSED), ↵ link and ⇧↵ link with a relation, CURRENT unlink and relabel, Tab marks, ID prompts, the consequence strip, and Ctrl+Shift+P on a LINKS line opening the owner's stage.

## Notes

[2026-10-20T15:32:35Z · bob-cli-a2.11] PROPOSED FOLLOW-UP: bob-cli just docs-check template tests test_templates_in_material and test_component_chips_in_material fail identically on clean origin/master (mkdocs absent in this env); unrelated to nav-links-stage

[2026-10-20T15:32:42Z · bob-cli-a2.11] PROPOSED FOLLOW-UP: 6 npm test failures reproduce identically on clean origin/master and are tracked in bob-cli-a2.9 note #2 (4 unblocked-glyph, 1 decision-card Keep, 1 forward-promotion); nav-links-stage adds 19 passing tests and changes none of those outcomes

[2026-10-20T15:35:41Z · bob-cli-a2.11] nav-links-stage landed in bob-plugins f50107e (nav-hotkeys 2.49.0): Task Card links-to row (312, l keycap, detail N-first-label-target-+K), Ctrl+Shift+L task-card-links chord (no core/vault conflict), Links stage 304/305/426/427 (CURRENT/RESULTS/CLOSED, relation field with index suggestions, Tab marks, ID prompts, strip), LINKS-line redirect via 300/550 (LG8), api.relations openStage for to-direction at v0. Tests: new test-navigation-relation-links-stage.cjs 19 pass (LG1-LG6, LG8, LG13, LG15); full npm test 3354 pass with only the 6 failures verified identical on clean origin/master (tracked in a2.9 note 2); docs template gate 2 failures also identical on clean base (follow-up noted). build:check, validate 7/7, docs inventory all green. Deployed via bob plugins sync (vault main.js/manifest byte-identical). Merged parallel chips phase 03bb94b (kept both sides in package.json/index.md; relations page section added to their new task-relations.md). No new disk reads on keystroke; pool reuses buffer/cache/chunked-scan machinery.

## Dependencies

- **Blocks:** [bob-cli-a2.12](bob-cli-a2.12.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a2.8](bob-cli-a2.8.md) ✓ · ⧖ 2026-10-20
- **Depends on:** [bob-cli-a2.9](bob-cli-a2.9.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a2.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.11/README.md) | [bob-cli-a2.11](bob-cli-a2.11.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a2.12][1] | Check the closed prerequisite's deliverables before building the reverse stage | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a2.12/README.md

<!-- sase:referenced-by:end -->
