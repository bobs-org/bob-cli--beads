# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2 — Mirror the remaining ledger-tools mark gates into popout windows

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2` · **Size:** medium
**Created:** 2026-10-26 10:47:09 EDT · **Closed:** 2026-10-26 12:20:00 EDT
**Plan:** [202610/backlog\_batch13\_vault\_integrity\_and\_perf\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch13_vault_integrity_and_perf_1.md)

## Description

popout-mark-gates: resolve bob-cli-cb by routing priority, task-tag, freshness, and Today-off body classes through the shared popout mirror, testing both toggle states, and deploying after the ignore fix.

## Notes

[2026-10-26T16:20:00Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2] Routed bob-priority-marks, bob-task-tag-marks, bob-fresh-marks, and bob-today-marks-off through BobLedgerToolsMarkGateMixin (applyMarkGateClass + registerMarkGatePopoutSync; off-class passes !enabled). Added one holds-in-popout test per family covering both toggle states. npm run build, npm test (3739 pass, 0 fail), npm run validate all green. Deployed bob-ledger-tools 1.73.0 via bob plugins sync after vault-plugin-ignore landed; bob-dep-chips has no CSS body gate so stayed out of scope. Target task bob-cli-cb left open for the lander; bob-plugins changes left uncommitted for the lander.

## Dependencies

- **Depends on:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.1.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@756a368`](https://github.com/bobs-org/bob-plugins/commit/756a3683fc3724d56c3e976a6c221f7daab280d9) | feat(ledger-tools): mirror priority, task-tag, freshness, and today-off mark gates into popout windows | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2.md) | 2026-10-26 12:21:11 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2/README.md

<!-- sase:referenced-by:end -->
