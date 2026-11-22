# Bead: bob-cli-on.6.1.4 — Requirements added to existing tasks, the scoop, and req\_link

[Bead Pages](../README.md) / [bob-cli-on.6.1](bob-cli-on.6.1.md) / bob-cli-on.6.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.6.md) · **Assignee:** `bob-cli-on.6.1.4` · **Size:** medium
**Created:** 2026-11-21 13:50:30 EST · **Closed:** 2026-11-21 21:22:12 EST
**Plan:** [202611/capture\_req\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_req_bullets.md)

## Description

existing-target-writes: write note-less @route+id requirement bullets and the same-line `[ ] text @route+id` form through insert_reqs with the first-requirement scoop, refuse forced-drawer reqs and Task Links to req anchors (req_link), and preview the scoop.

## Notes

[2026-11-22T02:05:50Z · bob-cli-on.6.1.4] PROPOSED FOLLOW-UP: Reconcile the first-req NOTES scoop with ^prj section filing — A capture to an existing ^prj that adds both a requirement and a note can create duplicate ## NOTES sections; fix the section routing and verify the loose-note scoop remains single and previewed.

[2026-11-22T02:10:51Z · bob-cli-on.6.1.4] PROPOSED FOLLOW-UP: Refresh stale documentation contract checks — On both the working tree and a clean archive of HEAD, tools/docs/tests/test_contracts.py has three failures: the registry count expects 54 rather than the current 55, the llms.txt contracts list omits task-requirements.md, and the README contract table hash is stale. Update those expectations as the contract index changes.

[2026-11-22T02:22:12Z · bob-cli-on.6.1.4] Implemented capture inserts for existing task requirements: same-line and grouped req bullets append under reqs, first-req scoops only pre-existing loose notes, same-draft notes file in NOTES, and requirement-anchor Task Links return req_link guidance. Focused coverage and full 'sase tool run check' passed; git diff --check passed. Recorded clean-HEAD-reproducible stale docs contract-index assertions and the ^prj NOTES section interaction as proposed follow-ups.

## Dependencies

- **Depends on:** [bob-cli-on.6.1.3](bob-cli-on.6.1.3.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.6.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.4/README.md) | [bob-cli-on.6.1.4](bob-cli-on.6.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3ce97d7`](https://github.com/bobs-org/bob-cli/commit/3ce97d736056fdf78ab3435badb3a03888842953) | feat(capture): write requirements to existing tasks | [bob-cli-on.6.1.4](bob-cli-on.6.1.4.md) | 2026-11-21 21:23:31 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.6.1.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.6.1.4/README.md

<!-- sase:referenced-by:end -->
