# Bead: bob-cli-on.11.1 — Obsidian requirement close card and carry-now

[Bead Pages](../README.md) / [bob-cli-on.11](bob-cli-on.11.md) / bob-cli-on.11.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.md) · **Assignee:** `bob-cli-on.11.1.land`
**Created:** 2026-11-22 14:59:30 EST
**Plan:** [202611/obsidian\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_requirement_close_card.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/obsidian_requirement_close_card.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_requirement_close_card.md

<!-- sase:links:end -->

## Description

Complete bob-cli-on.11 with guarded requirement carry, successor picker v6, ordered verdict writes, one Undo, and final jump landing across managed Done gestures.

## Notes

[2026-11-23T00:58:01Z · bob-cli-on.11.1.land] LAND TRIAGE (follow-ups): every PROPOSED FOLLOW-UP on the six phases (.1 #1, .2 #1, .3 #1, .5 #2, .6 #1) is one of two already-tracked 25 ms wall-clock flakes under full npm test load: event-link-times -> bob-cli-km, frees-marks -> bob-cli-io. Recorded attributed notes on both. No +1 because the lander did not reproduce them, and no new task beads. No other distinct follow-up was proposed.

[2026-11-23T00:58:05Z · bob-cli-on.11.1.land] LAND VERIFICATION (incomplete; remaining work is epic work, caused by close_wiring c91ebae). Reproduced against the bob-plugins master harness (55bf2ed): (1) applyManagedReqCloseCard passes picker reqs [{key,verdict,reason}] straight to reqCloseResolveVerdicts, which reads request.selector, so every explicit Drop/Carry/Carry+pull-in from the Obsidian card refuses req_close_stale (selectors ['undefined']); only implicit Met works. (2) resolveManagedReqCloseLanding hands an async reader to the synchronous resolveReqLanding (198f), so every requirement Ctrl+J pin returns req_jump_lost. moved_with_ancestor landings also lack exact text and use a 1-based line. (3) expectedNotes and expectedOwnerPostimages are derived from the same live text at apply time, so external owner-block edits made while the card is open (new req, sibling or title or note edit) are accepted. The plan requires req_close_stale. (4) cycleTaskStatusRange calls captureReqCloseOwnersFromText without identities, and that branch loops over tasks as if they were match arrays, so counted-range closes capture 0 owners. (5) Idless owners never reach finalizeClosedTasks (closedTaskIdentity returns null), so an unanchored owner with Pending reqs never opens the card. (6) The required public-path integration matrix and the real-Obsidian close-card e2e are missing: test-task-status-cycler-req-close-integration.cjs has 6 unit-level tests and obsidian-task-reqs-e2e.cjs has no card scenario. (7) Docs: bob-cli docs/task-requirements.md section 5 says Ctrl+Shift+T on a req keeps ordinary split, but nav carries via api.taskSplit. Section 7 does not describe the Obsidian card's receipts, Undo, Esc, or same-day reopen. docs/task-status-cycler.md has no close-card section. Verified OK: SP1-SP51/RV vectors, the twin parity and 101 focused req-close/carry tests pass, both plugins are deployed and synced (nav 2.107.0, cycler 1.58.1), there are no epic-symbol entries, and commits since the epic began (55bf2ed/7f104e52 Pomodoro mention history, 9d0cbfbe Mac card docs, ledger-tools/props/gmail/tick/highlights) neither conflict with nor duplicate this epic.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.11.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.land.md) | [bob-cli-on.11.1](bob-cli-on.11.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.11.1.2][1] | Need epic DECISIONS, phase graph, and design file for req_model work | 1 |
| read-by | [agent:bob-cli-on.11.1.4][2] | Need DECISIONS section | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.4/README.md

<!-- sase:referenced-by:end -->
