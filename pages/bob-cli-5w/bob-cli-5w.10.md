# Bead: bob-cli-5w.10 — Reopen takes successors back; Alt+\] closes join the pass

[Bead Pages](../README.md) / [bob-cli-5w](README.md) / bob-cli-5w.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0p.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0p.linker.w0.md) · **Assignee:** `bob-cli-5w.10` · **Size:** medium
**Created:** 2026-10-09 11:54:16 EDT · **Closed:** 2026-10-09 13:37:21 EDT
**Plan:** [202610/successor\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_links.md)

## Description

cycler_polish: in task-status-cycler, add an in-memory reopen receipt: reopening a predecessor removes its untouched successor links and restores their status. Route Alt+]/Alt+[ closes through finalizeClosedTasks (bead bob-cli-3k); cancels recover only. Ships tests, versions, a README update, and a sync.

## Notes

[2026-10-09T17:31:36Z · bob-cli-5w.10] PROPOSED FOLLOW-UP: record decisions strand closed-task-hands-slot-to-successors (epic decision decision_record=no skipped it; applies to bob-cli, bob-plugins, Bob Mac Capture)

[2026-10-09T17:31:40Z · bob-cli-5w.10] PROPOSED FOLLOW-UP: add glossary strand successor-link (epic decision glossary_term=no skipped it; link to task-link and task-dependency-link)

[2026-10-09T17:31:45Z · bob-cli-5w.10] PROPOSED FOLLOW-UP: full bob-plugins npm test has 2 pre-existing date-sensitive failures in test-navigation-roll-decay.cjs (picker-single P2 roll) reproducing identically on the clean base; tracked by task bead bob-cli-5r, plus a flaky ranker perf test that passes in isolation

[2026-10-09T17:37:12Z · bob-cli-5w.10] PROPOSED FOLLOW-UP: just check stays red on 9 pre-existing highlights_ref::return_links filter failures, identical on the clean base tree (already noted on bob-cli-5w.2)

[2026-10-09T17:37:21Z · bob-cli-5w.10] cycler_polish shipped in bob-plugins (cycler 1.29.0): in-memory reopen receipt (new 136 fragment; same-day Ctrl+Enter reopen takes back untouched successor links, restores statuses, shows the take-back notice; edited lines survive; capture closes gain no receipt) and Alt+]/Alt+[ closes routed through finalizeClosedTasks (bare, counted batched, transcluded-target; Cancelled uses closeKind cancelled, recover-only rows report cancelled; closes bob-cli-3k). Verified: new successor-polish suite 7/7, all 265 cycler tests green, npm run validate green, bob plugins sync done, epic-symbols clean. just check red only on 9 pre-existing return_links failures identical on base (noted on 5w.2); full plugin suite only adds 2 pre-existing decay failures tracked by bob-cli-5r plus a flaky ranker perf test green in isolation. Memory untouched per epic DECISIONS (2 PROPOSED FOLLOW-UPs recorded).

## Dependencies

- **Blocks:** [bob-cli-5w.11](bob-cli-5w.11.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5w.8](bob-cli-5w.8.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5w.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5w.10/README.md) | [bob-cli-5w.10](bob-cli-5w.10.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`08da012`](https://github.com/bobs-org/bob-cli/commit/08da0125d9fca0d6f05f5598b35deed1a57de62e) | docs(hooks): option-bracket closes join the successor pass; same-day reopen takes links back | [bob-cli-5w.10](bob-cli-5w.10.md) | 2026-10-09 13:39:01 EDT |
| bob-plugins | [`bob-plugins@22e96a3`](https://github.com/bobs-org/bob-plugins/commit/22e96a32bae18560e259a734f2ebb3150ca78003) | feat(task-status-cycler): same-day reopen takes back successors; Alt+\]/Alt+\[ closes join the pass | [bob-cli-5w.10](bob-cli-5w.10.md) | 2026-10-09 13:43:52 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5w.10][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5w.10/README.md

<!-- sase:referenced-by:end -->
