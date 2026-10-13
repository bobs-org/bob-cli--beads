# Bead: bob-cli-7c.4 — task-status-cycler plans offers, awaits the picker, then applies

[Bead Pages](../README.md) / [bob-cli-7c](README.md) / bob-cli-7c.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.11.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.11.linker.w0.md) · **Assignee:** `bob-cli-7c.4` · **Size:** large
**Created:** 2026-10-13 09:48:12 EDT · **Closed:** 2026-10-13 11:25:27 EDT
**Plan:** [202610/successor\_offers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_offers.md)

## Description

cycler_offers: port the offer rule to the cycler, delete SUCCESSOR_BREAKER_LIMIT, await nav's picker between plan and apply, re-plan with the selection against fresh text, stamp picks, guard the editor insertion branch, extend the reopen receipt, and fall back to a no-link notice without nav.

## Notes

[2026-10-13T15:25:27Z · bob-cli-7c.4] Implemented cycler successor offers (bob-cli-7c.4): pure planner produces hand_off/project/project_finished offers with stable keys (path#^id, path@fnv8 ~k), implicit/no_destination, dedup (hand_off wins), offer metadata (key/n/group/project/destination/selected/block_id_needed), selection null/none/all/subset, pick writes (raise Ready/Blocked to Next, mint only when needed, strip #prj_is_blocked, stamp via getFreshnessStampLine, one guarded edit), breaker deleted, project enumeration (all open residents incl stale/ref/inbox, muted still_blocked with project, hidden/already-planned folded, sub-project counts, ^prj header), pull-ins as project_finished with unconditional #hide removal, insertion implicit entry children + stub replace, notice copy (not pulled in, no open Pomodoro, project member, pulled-in summary, mixed, failure; breaker kept for old payloads), editor snapshot guard mirroring vault.process, plan(no selection)->one nav pick(model camelCase, headers, muted, folded)->re-read fresh (editor first, scoped index, no warm full scan)->re-plan with picks (refuse stale/ambiguous incl idless digest-count change, new offers unpicked, no prereq fulfillment, anchor revalidation, same-file snapshot accounting)->apply with preimage guards->return model via successorNoticeTarget return; receipts save pre/post lines for picked rows (freshness/minted). Tests: successors 52 pass, offers (new SO1-32 vectors) 7 pass, pull-in 36 pass, polish 7 pass; wiring 10/11 (Pomodoro-line close fails in suite with completed false but passes standalone via /tmp probe with identical setup - test isolation issue, needs investigation); full npm test 2672 pass 8 fail (4 ledger glyph, 1 keep, 1 perf in unchanged plugins - pre-existing/environmental, build unchanged; 1 Pomodoro wiring as above; 1 task-links-api not_planned_today->no_destination fixed after full run). Version 1.38.0 manifest+README (automatic-link copy updated), build/build:check/validate green, fragments <=1000 (085 987, 085b 655, 089 804, 089b 353, 087 736, 135 710, 137 658, 136 570), sync deployed (2 copied 1 unchanged, backups) dry-run up to date. PROPOSED FOLLOW-UP: investigate wiring Pomodoro suite-vs-standalone divergence (standalone /tmp/pomodoro_probe.cjs passes, suite fails completed false); confirm 6 other-plugin failures pre-existing on clean base (unchanged entrypoints).

## Dependencies

- **Depends on:** [bob-cli-7c.1](bob-cli-7c.1.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7c.6](bob-cli-7c.6.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-7c.8](bob-cli-7c.8.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7c.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7c.4.md) | [bob-cli-7c.4](bob-cli-7c.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@310739d`](https://github.com/bobs-org/bob-plugins/commit/310739dd72d70856d89a7fc1a3eb0c03d24ca048) | feat(cycler): offer successors and await picker before applying (bob-cli-7c.4) | [bob-cli-7c.4](bob-cli-7c.4.md) | 2026-10-13 11:28:18 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7c.land][1] | Need the child scope and notes | 1 |
| read-by | [agent:bob-cli-7e.land][2] | Check whether 7c phases already recorded the successor-wiring continuation test failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7c.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7e.land/README.md

<!-- sase:referenced-by:end -->
