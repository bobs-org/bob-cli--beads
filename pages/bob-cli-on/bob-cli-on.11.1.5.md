# Bead: bob-cli-on.11.1.5 — Place carried tasks and resolve final requirement landings

[Bead Pages](../README.md) / [bob-cli-on.11.1](bob-cli-on.11.1.md) / bob-cli-on.11.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.md) · **Assignee:** `bob-cli-on.11.1.5` · **Size:** medium
**Created:** 2026-11-22 14:59:31 EST · **Closed:** 2026-11-22 17:01:38 EST
**Plan:** [202611/obsidian\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_requirement_close_card.md)

## Description

req_delivery: adapt successor placement for carried tasks without freshness stamping and resolve requirement pins through composed move maps and final note routing.

## Notes

[2026-11-22T22:01:23Z · bob-cli-on.11.1.5] Verified req_delivery: cycler pull-in placement (198e) + pin resolver (198f); RV29-RV43 exact bytes via plan/apply adapters; npm test 8798 pass / 1 unrelated flaky perf (passes alone) / 17 perf pass; build+docs-inventory clean; deployed task-status-cycler to vault (uncommitted build).

Apply-service seam for close_wiring:
- helpers.createReqPullInPreflight({ day, dayPath, index, completed, closing, today? }) -> pullInPreflight({ owners, verdicts, notes }) closure for planReqCloseWrites/applyReqCloseWrites. day = staged post-close day text or null; completed = [{ path, blockId, isRoot }]; closing = { continuationName, closedLine (0-based), continuation: { line (1-based), created } | null } | null. Refuses req_pull_in_no_destination before any write when a pulled carry has no slot/closing/implicit destination.
- helpers.planReqPullInLinks({ owners, outcomes, day, dayPath, index, completed, closing, notes, today?, routePulledTask?, settings? }) -> { ok, dayAfter, links[], notesAfter, postimages, restores[] }. Run on the apply result notes; merge with composeReqCloseRestores([...applyRestores, ...pullInRestores]) (earliest-before to final-after, incl. created inbox.md). Raises created tasks to Next with no freshness stamp; skips already-live links; refuses req_pull_in_no_destination / req_close_stale with nothing staged. routePulledTask is an optional D7 hook ({ task, taskLine, dayText, dayPath, target, destination, today }) -> { target, destination, routed } | { refusal }; without it destinations stay as resolved.
- helpers.resolveReqLanding({ target, owners, plan, routes, settings? }, finalText) -> { ok, landing: { key, kind: carried_task | moved_with_ancestor | requirement, outcome, path, line (1-based), blockId | null } }. Pin-only writes nothing. Refuses req_jump_lost / req_jump_ambiguous before commit; never navigates (close_wiring owns the final jump + receipt).
- Fragments 198e/198f are cycler-only (no nav twin copy); vectors.json fixture unchanged (byte-identical copy); new tests test-task-status-cycler-req-close-pull-in.cjs (14) + test-task-status-cycler-req-close-landing.cjs (12) registered in test:unit.

[2026-11-22T22:01:27Z · bob-cli-on.11.1.5] PROPOSED FOLLOW-UP: perf flake test-ledger-tools-event-link-times.cjs "one build over a 200-link ledger stays under 25 ms" failed once under full-suite load (43.5ms) and passes alone; unrelated to req_delivery.

[2026-11-22T22:01:38Z · bob-cli-on.11.1.5] req_delivery verified: RV29-RV43 exact bytes, 26 new tests green, full plugin suite 8798 pass (1 unrelated perf flake, passes alone), deployed to vault

## Dependencies

- **Depends on:** [bob-cli-on.11.1.4](bob-cli-on.11.1.4.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-on.11.1.6](bob-cli-on.11.1.6.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.11.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.5/README.md) | [bob-cli-on.11.1.5](bob-cli-on.11.1.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.11.1.5][1] | check phase notes and remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.5/README.md

<!-- sase:referenced-by:end -->
