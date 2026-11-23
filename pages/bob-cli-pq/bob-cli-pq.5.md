# Bead: bob-cli-pq.5 — The Mac draft shows requirement bytes as a teal chip

[Bead Pages](../README.md) / [bob-cli-pq](README.md) / bob-cli-pq.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1f8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1f8.md) · **Assignee:** `bob-cli-pq.5` · **Size:** medium
**Created:** 2026-11-23 03:54:18 EST
**Plan:** [202611/task\_reqs\_criterion\_diamond.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_reqs_criterion_diamond.md)

## Description

mac-editor: Bob Mac Capture deletes the hash overlay, the byte concealment, and its caret-reveal plumbing, and paints the real `[ ]` bytes as a teal chip like the existing route and theme washes.

## Notes

[2026-11-23T10:27:39Z · bob-cli-pq.5] SEQUENCING WAIT: Approved plan step 0 requires bob-cli-ph.7 and bob-cli-ph.8 to land before Mac editor changes; both are still in_progress. Linked Mac checkout is clean at 0b458fb1 and still has RequirementMarkerGlyphOverlay and caret concealment, so this phase has not landed. No implementation edits made. Resume after both prerequisites close, refresh the linked checkout through sase repo open, read the required research companions, and implement the mac-editor scope.

[2026-11-23T15:14:40Z · bob-cli-pq.5] SEQUENCING WAIT: Rechecked approved plan step 0 and both prerequisites on 2026-11-23; bob-cli-ph.7 and bob-cli-ph.8 are still in_progress. Refreshed bob-mac-capture through sase repo open; clean origin/master remains 0b458fb1 with RequirementMarkerGlyphOverlay, concealedRequirementMarkerSpans, and refreshRequirementMarkerConcealmentIfNeeded intact. This phase has not landed and no implementation changes were made. The original bounded mac-editor scope still fits one coding agent. Staging an automatic prerequisite monitor; successor must verify both resolutions, refresh the linked checkout, read all three research companions, implement the chip and tests/docs, run Mac gates, resolve epic symbols, and close only bob-cli-pq.5.

## Dependencies

- **Depends on:** [bob-cli-ph.7](../bob-cli-ph/bob-cli-ph.7.md) ◐ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-ph.8](../bob-cli-ph/bob-cli-ph.8.md) ◐ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pq.6](bob-cli-pq.6.md) ◐ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-pq.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-pq.5.md) | [bob-cli-pq.5](bob-cli-pq.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1fk][1] | Research whether pq.3/pq.5 truly depend on bob-cli-ph | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.1fk/README.md

<!-- sase:referenced-by:end -->
