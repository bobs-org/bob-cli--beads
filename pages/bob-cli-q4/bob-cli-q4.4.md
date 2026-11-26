# Bead: bob-cli-q4.4 — Reconcile drift meter and recorded baseline

[Bead Pages](../README.md) / [bob-cli-q4](README.md) / bob-cli-q4.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fw](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fw.md) · **Assignee:** `bob-cli-q4.4` · **Size:** medium
**Created:** 2026-11-25 08:51:35 EST · **Closed:** 2026-11-25 12:54:15 EST
**Plan:** [202611/better\_o\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/better_o_gesture_settle.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | [bead:bob-cli-qd][1] | Holds the 7-day reconcile-drift baseline table and JSON attachment to compare against |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-qd/README.md

<!-- sase:links:end -->

## Description

drift-meter: add `scripts/dev/reconcile-drift`, which replays vault commits through `bob task reconcile --dry-run -f json` with `BOB_NOW` pinned. It sorts the planned changes into churn categories, attributes them to gestures, and reports tidy debt. Record today's baseline on the phase bead.

## Notes

[2026-11-25T17:53:47Z · bob-cli-q4.4] 7-day reconcile-drift baseline (2026-11-25, vault ~/bob, since '7 days ago', -j 8, bob 0.6.0).
1851 commits considered, 1800 replayed, 50 unchanged; 1 replay error continued.
Window 2026-11-18 → 2026-11-25 America/New_York. JSON: 🔒 reconcile-drift-baseline.json

Category                         Introduced
status-group move                      1007
badge row                                75
local schedule flip                       0
recurring spawn flip                     88
LINKED FROM mention strip                53
midnight wake or unblock                239
ledger hygiene                           77
dependency or field healing              93
other                                    18
total                                  1650

By morning
Day          Review  Commits   group   badge   sched   recur mention    wake  ledger    deps   other
2026-11-18   no           60      15       7       0       0       0       0       1       0       0
2026-11-19   yes         224     105      13       0      10       4       1       9       1       0
2026-11-20   yes         284     191      13       0      13       5      81      16      72      17
2026-11-21   yes         291     146       9       0      11      12      40       7       3       0
2026-11-22   yes         307     166      10       0      15       8      31      21       5       0
2026-11-23   yes         254     212      11       0      16      10      36      12       8       1
2026-11-24   yes         267      70       5       0      10       1      29       6       2       0
2026-11-25   yes         164     102       7       0      13      13      21       5       2       0

Top gestures by introduced churn
midnight_rollover                                              8 commits, 347
pre:checklist                                                 40 commits, 171
vault(kellys-macbook-pro-local): 1 file - sase_blog.md        20 commits, 143
vault(kellys-macbook-pro-local): 1 file - bob.md             266 commits,  90
tickler:drop                                                   8 commits,  66
tickler:defer                                                 33 commits,  64
new:done                                                      39 commits,  42
new:today                                                      5 commits,  40
post:checklist                                                14 commits,  38
vault(apollo): 1 file - sase_blog_drafts.md                    1 commit,   31

Tidy at window end: 602 open tasks in 5822 notes scanned, 0 tidied
Outstanding planned reconcile changes: 2 (status-group move 1, ledger hygiene 1)

Replay error (run continued): fe37799c05d3 bob task reconcile exit 1: daily note has no Pomodoros section (2026/20261123.md in that snapshot).

[2026-11-25T17:53:59Z · bob-cli-q4.4] PROPOSED FOLLOW-UP: just docs-check fails on pre-existing docs/reference/plugins/bob-navigation-hotkeys.md over budget (6068 vs cap 6000); this phase does not touch that page.

[2026-11-25T17:54:04Z · bob-cli-q4.4] PROPOSED FOLLOW-UP: reconcile-drift records a replay error when the snapshot daily note exists but has no Pomodoros section (fe37799c05d3, 2026/20261123.md); 1 of 1801 replays in the 7-day baseline.

[2026-11-25T17:54:15Z · bob-cli-q4.4] Added scripts/dev/reconcile-drift with fixture tests and docs/develop/reconcile-drift.md. python3 -B scripts/dev/test_reconcile_drift.py (15 tests) and just check-scripts passed. 7-day ~/bob baseline: 1851 commits, 1800 replayed, 50 unchanged, 1650 introduced (1007 status-group moves), tidy 0 of 602 open tasks. No --epic-symbol leftovers.

## Attachments

- 🔒 reconcile-drift-baseline.json · application/json · 710.872 KiB (private attachment)

## Dependencies

- **Blocks:** [bob-cli-q4.13](bob-cli-q4.13.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.4/README.md) | [bob-cli-q4.4](bob-cli-q4.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e532b11`](https://github.com/bobs-org/bob-cli/commit/e532b11f911486e404fefeed3c7a7653dd7cbef7) | feat(dev): add reconcile-drift vault replay meter | [bob-cli-q4.4](bob-cli-q4.4.md) | 2026-11-25 12:55:36 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.4][1] | Need notes, design file path, and remaining work from earlier agents | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.4/README.md

<!-- sase:referenced-by:end -->
