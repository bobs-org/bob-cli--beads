# Bead: bob-cli-g1 — Ledger frees marks

[Bead Pages](../README.md) / bob-cli-g1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.176](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.176.md) · **Assignee:** `bob-cli-g1.land`
**Created:** 2026-11-02 12:45:29 EST · **Closed:** 2026-11-02 16:28:54 EST
**Plan:** [202611/ledger\_frees\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ledger_frees_marks.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/ledger_frees_marks.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:1c86942de5e48357b13f472a | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ledger_frees_marks.md

<!-- sase:links:end -->

## Description

In today's daily note, each Task Link under an open Pomodoro whose task is the last blocker of other open tasks wears a quiet "🔑 frees N" mark. N always matches the task's own BLOCKS row, the hover names the freed tasks, and the mark is verified in real Obsidian.

## Notes

[2026-11-02T20:43:15Z · bob-cli-g1.land] FOLLOW-UP TRIAGE completed before proposing the remaining-work tale. Reviewed every note on bob-cli-g1.1 (1), g1.2 (4), and g1.3 (2).
- g1.2 #1 generated glossary: declined as resolved. Current npm run docs:check passed all implemented gates, 447 tests with one skipped. The later CLI docs regeneration 8c140e43 is present. No new glossary task.
- g1.2 #2 and g1.3 #1 baseline failures: independently reproduced seven failures on unchanged bob-plugins a28d1af under America/New_York (110/117 pass), and added +1 evidence to existing tasks bob-cli-f8 (snapshot/order 103.1ms >50ms and rank 16.5ms >12ms), bob-cli-et (freshness due-set reload), bob-cli-f7 (12:30 vs 16:30), bob-cli-eh (note-ready 1 vs 2 and relation-index layout-ready), bob-cli-ff (2026-11-02 no longer future). Evidence file:explicit:1c86942de5e48357b13f472a. Same-type search, last-week CI task sweep, and active-epic scope sweep found semantic duplicates and no causally related active epic. No new tasks.
- g1.2 #3 rebase/sync: retained as this epic's integration work, not a separate follow-up. Source a28d1af incorporates 289f764, 93d3859 and d42b951. BUT explicit-repo bob plugins list still reports ledger-tools drift; vault stamp is uncommitted f824dd1 from g1.3 at 20:29:03Z. A no-pull dry run shows vault manifest 1.92.0 versus source 1.93.0 and main.js/styles.css differences. The repair tale must deploy the repaired combined source and verify synced; phase 3's forced deploy did not finish this integration.
- g1.2 #4 Chromium timeout: note reports an isolated passing rerun, and g1.3's isolated e2e later passed; no independent persistent failure observed during this review, so no additional task filed. The deterministic seven failures above remain tracked separately.
The compact pill decision was honored. No epic-symbol entries currently exist. The parent-link read shows no parent_bead.

[2026-11-02T20:43:16Z · bob-cli-g1.land] LANDING VERIFICATION: Do not close yet. Reviewed actual plugin pure model, mixin, shared BLOCKS helpers, lifecycle wiring, CSS, vectors, real-Obsidian harness and contract; reviewed CLI commits b508f0b6/07edcdfa and plugin f824dd1/a28d1af. Intervening CLI capture relations, Pomodoro merge and GCal commits do not change the explicitly dependency-only frees rule. Plugin block-reason/chip commits 289f764/93d3859/d42b951 are integrated in source but not in the deployed build (see triage note).
Remaining epic-caused defects reproduced with the existing test harness helpers on a28d1af:
1. buildFreesMarkDecorations uses dailyPath + blockId for count history. Owners one.md#^prj (count 1) and two.md#^prj (count 2) give first-paint tick false/true and unchanged second-build true/true. Use resolved owner path+blockId and per-build transitions.
2. refreshFreesMarksForRollover updates freesMarkDay before refreshFreesMarksEditors filters leaves to the new date. With yesterday open, rollover returns true and dispatches ZERO refreshes to that editor, leaving stale marks. Refresh yesterday as well.
3. FreesMarkWidget.eq returns true for different linktext one#^prj versus two#^prj with identical blockId/count/tooltip, preserving the old Mod-click closure after retargeting. Include navigation identity.
4. Approved unique-target render caching and 200-link/2000-task performance test are missing. Probe of 200 identical target rows/2000 tasks makes 200 owner-count lookups, elapsed 10.56ms; target/count work precedes viewport filtering.
5. E2e tick-count-updates waits 4s but prints within=1s; tick-class-once accepts two records, and caret check tests only the line. Tighten measurements/assertions to verify the actual contract.
Existing focused tests still pass 56/56, validate passes 8/8, docs gate passes 447/1 skipped. just check was not run during this read-only source audit; the repair coder must run it, never check-full. A validated medium tale, Finish ledger frees marks and land bob-cli-g1, covers only these repairs, integrated deployment, truthful live verification, and final normal epic closure plus plan status done. It has no land agent: its coder must finish the closeout without waiting for its own commit.

[2026-11-02T21:28:54Z · bob-cli-g1.land--3] Landing repairs for ledger frees marks closed normally.

Repairs in bob-plugins (uncommitted on a28d1af; generated main.js via npm run build, never hand-edited):
- Motion keys use the resolved owner path+blockId so distinct notes sharing ^prj no longer collide; transitions are computed once per owner per build.
- FreesMarkWidget.eq includes linktext and sourcePath so Mod-click follows a retargeted owner.
- Rollover refreshes all markdown leaves and clears count history; yesterday's marks drop without typing or scrolling.
- Per-build resolve/count caches plus visible-range skip; unique-target work runs once per build.
- E2e timing 1000ms+500ms, exact caret column, and one animation burst (shared across visible FC1 rows).

Reviewed commits: CLI b508f0b6/07edcdfa (contract + live verification); plugin f824dd1/a28d1af plus d42b951 miniatures (and 289f764/93d3859) preserved. Compact pill_text=compact holds (visible 🔑 N, tooltip says frees). Dependency-only count still matches BLOCKS. No parent_bead, so no ancestor close. sase bead epic-symbols bob-cli-g1 is empty. just symvision is unavailable (bob-cli has no recipe; bob-plugins has no Justfile). No memory or new CLI/API surface.

Passing checks:
- focused frees/BLOCKS/progress/unblocked/e2e-self-test 74/74 then 18/18 after the burst helper
- npm run build 0
- npm run validate 0
- BOB_CLI_DIR docs:check 447 passed, 1 skipped
- just check 0 and just docs-check 0 (monitor rkm05z3zx1bf)
- isolated xvfb-run /snap/bin/obsidian e2e 49/49 on the scratch vault: caret ch=16, count 1→2 in 322ms, one tick burst across four visible FC1 rows; light/dark Live Preview and Reading screenshots reviewed; docs/frees-marks.md records those measurements

Deploy: bob plugins sync --no-pull --repo the opened bob-plugins checkout --plugin bob-ledger-tools without --force. bob plugins list --no-pull --repo that checkout --format json: synced=8 drift=0; ledger-tools 1.93.0 uncommitted deploy from that checkout at 2026-11-02T21:13:41Z (source_head a28d1af).

Follow-up dispositions:
- g1.2#1 glossary: declined as resolved; docs gate passes
- g1.2#2 and g1.3#1: seven independently reproduced baseline npm-test failures remain out of scope and corroborated on bob-cli-f8 (two wikilink CPU budgets plus this run's cold-build sibling 16.5ms>16ms), bob-cli-et (freshness reload), bob-cli-f7 (Keep 12:30 vs 16:30), bob-cli-eh (note-ready 1 vs 2 and relation-index layout-ready), bob-cli-ff (2026-11-02 no longer future). Evidence file:explicit:1c86942de5e48357b13f472a
- g1.2#3 sync completed this landing
- g1.2#4 Chromium timeout is not an epic defect

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-g1.1](bob-cli-g1.1.md) | Authoritative display contract (bob-cli) | ✓ closed | small | 2026-11-02 | 1 | 1 |
| [bob-cli-g1.2](bob-cli-g1.2.md) | The mark in bob-ledger-tools (bob-plugins) | ✓ closed | medium | 2026-11-02 | 1 | 1 |
| [bob-cli-g1.3](bob-cli-g1.3.md) | Real-Obsidian e2e and visual review (bob-plugins, bob-cli) | ✓ closed | medium | 2026-11-02 | 1 | 2 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-g1: Ledger frees marks [closed]"]
    n1["bob-cli-g1.1: Authoritative display contract (bob-cli) [closed]"]
    n2["bob-cli-g1.2: The mark in bob-ledger-tools (bob-plugins) [closed]"]
    n3["bob-cli-g1.3: Real-Obsidian e2e and visual review (bob-plugins, bob-cli) [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n1 -.-> n2
    n2 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-g1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-g1.1/README.md) | [bob-cli-g1.1](bob-cli-g1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-g1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-g1.2.md) | [bob-cli-g1.2](bob-cli-g1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-g1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-g1.3/README.md) | [bob-cli-g1.3](bob-cli-g1.3.md) | 2 |
| [bbugyi200.athena.bob-cli-g1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-g1.land.md) | [bob-cli-g1](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b508f0b`](https://github.com/bobs-org/bob-cli/commit/b508f0b69dbd5dab08b7e6d1eb7c4c0f2ae1a01a) | docs(frees-marks): add ledger frees-mark display contract | [bob-cli-g1.1](bob-cli-g1.1.md) | 2026-11-02 12:58:52 EST |
| bob-plugins | [`bob-plugins@f824dd1`](https://github.com/bobs-org/bob-plugins/commit/f824dd1c1f32031e02421261c1a269d3ae262026) | feat(ledger-tools): show quiet frees-N marks after last-blocker ledger links | [bob-cli-g1.2](bob-cli-g1.2.md) | 2026-11-02 14:45:02 EST |
| bob-cli | [`07edcdf`](https://github.com/bobs-org/bob-cli/commit/07edcdfa646ec234e2efee28dee7a201801e9f66) | docs(frees-marks): record live verification | [bob-cli-g1.3](bob-cli-g1.3.md) | 2026-11-02 15:30:36 EST |
| bob-plugins | [`bob-plugins@a28d1af`](https://github.com/bobs-org/bob-plugins/commit/a28d1af8a5f647486b33ea4e41312aaf331fe36b) | test(ledger-tools): real-Obsidian e2e for frees marks | [bob-cli-g1.3](bob-cli-g1.3.md) | 2026-11-02 15:30:53 EST |
| bob-cli | [`4422abc`](https://github.com/bobs-org/bob-cli/commit/4422abcce2b8b972b96c860830ccbd3a1b1af1be) | docs(frees-marks): record measured live-verification timings | [bob-cli-g1](README.md) | 2026-11-02 16:30:36 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-g1.1][1] | epic decisions | 1 |
| read-by | [agent:bob-cli-g1.3][2] | Need epic DECISIONS and remaining notes for live_verify | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-g1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-g1.3/README.md

<!-- sase:referenced-by:end -->
