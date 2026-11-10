# Bead: bob-cli-iz.5 — Hold a replaced Events section and record the deletion policy

[Bead Pages](../README.md) / [bob-cli-iz](README.md) / bob-cli-iz.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1aa](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1aa.md) · **Assignee:** `bob-cli-iz.5` · **Size:** small
**Created:** 2026-11-09 07:12:09 EST · **Closed:** 2026-11-09 10:18:55 EST
**Plan:** [202611/gcal\_sync\_race\_force\_and\_skip\_reasons.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_sync_race_force_and_skip_reasons.md)

## Description

replaced_hold: bob-cli. When every row Bob wrote for the day and the Events stamp vanish together, do what the replaced_events decision says (default: hold with status `held`), update list/doctor/docs, and write the decision records. See plan section "Phase replaced_hold".

## Notes

[2026-11-09T15:18:55Z · bob-cli-iz.5] Implemented the replaced-Events held outcome, list/doctor reporting, forced recovery behavior, docs, and authorized decision records. Verified all gcal integration suites, cargo clippy --all-targets, cargo check --all-targets, and the replaced-section recovery test. just docs-check could not run because the mounted bob-mac-capture checkout resolves to the primary repo instead of its own Git worktree.

[2026-11-10T02:06:01Z · bob-cli-iz.land] LANDER NOTE (bob-cli-iz.land): this phase's commit (feat(gcal)!: hold replaced Events sections, rebased as 9a0bb25c) never reached bob-cli master. Workspace bob-cli_10's origin had been rewritten to bob-mac-capture (see bob-cli-jf), so the commit was pushed onto bob-mac-capture's master instead. The lander re-applied the full diff (sync/list/doctor/skip held outcome, tests, docs, and the authorized decision-memory edits, regenerated with sase memory init) onto bob-cli 12692ebb and committed it from the land turn.

## Dependencies

- **Depends on:** [bob-cli-iz.4](bob-cli-iz.4.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-iz.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-iz.5/README.md) | [bob-cli-iz.5](bob-cli-iz.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-iz.5][1] | Need phase notes and any recorded remaining work | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-iz.5/README.md

<!-- sase:referenced-by:end -->
