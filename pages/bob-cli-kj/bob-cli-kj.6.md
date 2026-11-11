# Bead: bob-cli-kj.6 — Task-wikilink CPU budget investigation

[Bead Pages](../README.md) / [bob-cli-kj](README.md) / bob-cli-kj.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bm](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bm.md) · **Assignee:** `bob-cli-kj.6` · **Size:** large
**Created:** 2026-11-11 17:20:04 EST · **Closed:** 2026-11-11 18:15:08 EST
**Plan:** [202611/impact\_ranked\_bead\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/impact_ranked_bead_fixes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:0fbe7c60257f385fa8ed7df5 | attached via sase artifact create --bead |
| related | file:explicit:176518f8978d9d148be86a5f | attached via sase artifact create --bead |
| related | file:explicit:852c774f2f1b00df676ba605 | attached via sase artifact create --bead |
| related | file:explicit:8837ecf4a57e2fa55bf54437 | attached via sase artifact create --bead |
| related | file:explicit:a4eb719bfd4855535901ea2d | attached via sase artifact create --bead |
| related | file:explicit:c96e49fd9445fc49193f339a | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

wikilink-perf: establish reproducible measurements for the block-id-prompt task-wikilink snapshot/order and keystroke-rank CPU budget failures, then land a production fix, measurement fix, or justified budget — never a silent bump (bead bob-cli-f8).

## Notes

[2026-11-11T22:41:17Z · bob-cli-kj.6] PLANNING EVIDENCE: No earlier phase notes or landed repair found; bob-plugins e8a776ee909e38aaeb2031e26197b6dc0522189e retains the f0c1c97 ranker/test and original index decoration. Unmodified focused test on athena Node v20.19.2: 3/5 pass, snapshot/order 74.4 ms > 50 and rank 13.9 ms > 12. Identical source bytes evaluated through SSH stdin on apollo Node v18.19.1: 3/5 pass, 95.2 ms and 16.8 ms respectively; no remote repo reads or writes. Both use process.cpuUsage fallback, not thread CPU. In-memory ablations implicate spread-plus-appended snapshot row properties and cached search-field order: fresh Object.assign copy plus search-text-first fields yielded snapshot/order 18.56–30.76 ms and rank 1.32–11.22 ms over seven sequential samples. A fresh athena process using only that decorateRow substitution passed the original 5/5 performance tests. Source/test files remain unchanged. A medium tale is validated for the local production repair, real cached-versus-uncached parity tests, profiling, repeated cross-host controls, full gates and sync; implementation is deferred only to the explicitly requested plan approval, not an oversized unfinished coding attempt. No epic-symbol entries currently exist. Preliminary measurements are not final acceptance evidence.

[2026-11-11T23:15:03Z · bob-cli-kj.6] VERIFICATION: Warm snapshot/rank CPU budgets restored without raising 50 ms / 12 ms / 16 ms / 1.5 s limits. Cause was V8 hidden-class deopt from spread-plus-appended decorateRow plus original-order cached search fields. Repair is Object.assign fresh copy plus search-text-first loweredTaskWikilinkSearchFields; decoration stays snapshot-local.

Report: file:explicit:c96e49fd9445fc49193f339a
Raw measurements: file:explicit:852c774f2f1b00df676ba605
Athena before/after: file:explicit:8837ecf4a57e2fa55bf54437 file:explicit:176518f8978d9d148be86a5f
Apollo before/after (reproducing host, Node v18.19.1, process.cpuUsage): file:explicit:a4eb719bfd4855535901ea2d file:explicit:0fbe7c60257f385fa8ed7df5

Apollo TAP before: 3/5 × 3 (snapshot 94.8–113.6 ms, rank 15.0–17.7 ms). After: 5/5 × 3. Diagnostic snapshotPlusOrder 106.42/111.08/127.85 → 29.16/36.11/47.06 ms; queryRank 24.69/30.95/53.05 → 10.92/11.47/15.60 ms. Athena v22 already passed focused TAP before the repair; same-runtime after still 5/5 × 3.

Functional coverage: index metadata/cache-parity/overlay-rename-delete-refresh; model cached-vs-uncached with populated loweredSearchFields; picker runtime/view in both full npm test runs with no wikilink failures. build:check and validate passed. bob plugins sync --no-pull deployed block-id-prompt (backup 20261111-180121); no -F.

Cold-chunk: scheduled chunks stay under 16 ms; last-yield tail (endBatch basename rebuild) is 15.7–27.8 ms and is independent of decorateRow. Diagnostic now reports tailCpuMs.

PROPOSED FOLLOW-UP: parent docs_headroom owns npm run docs:check lint overruns (mac-capture pages and bob-navigation-hotkeys.md over 6000 words) plus strict Zensical missing bob-vim-yank-flash.md#verification, task-dependencies.md#1217-lp--leaf-vectors, and gcal.md#events.
PROPOSED FOLLOW-UP: cold-index last-yield tail ~21–28 ms (basename rebuild after the final yield) is omitted from TAP chunk samples; keep 16 ms scheduled-chunk contract, do not redesign cold index in this phase.
PROPOSED FOLLOW-UP: full-suite process-CPU contention still trips unrelated 25 ms mark budgets (event-link-times, frees-marks, keep-moving-marks-surface, off-clock-link-chips) and can trip the 50 ms snapshot budget at load ~32 (run 2: 80.0 ms). Isolated ledger tests 54/54 on clean HEAD and dirty tree; isolated wikilink TAP passes. Leave bob-cli-f8 and bob-cli-kj open.

[2026-11-11T23:15:08Z · bob-cli-kj.6] Verified on the final repair tree: Object.assign decorateRow plus search-text-first cached fields restores the 50 ms snapshot/order and 12 ms keystroke budgets without raising them. Apollo v18 TAP 3/5×3 before (snapshot 94.8–113.6 ms, rank 15.0–17.7 ms) and 5/5×3 after; diagnostic snapshotPlusOrder median 111→36 ms. Athena v22 focused TAP 5/5×3 after. Index/model/picker coverage, build:check, validate, and bob plugins sync succeeded. Evidence: file:explicit:c96e49fd9445fc49193f339a file:explicit:852c774f2f1b00df676ba605. Unrelated docs:check and full-suite 25 ms mark contention recorded as PROPOSED FOLLOW-UP. Left bob-cli-f8 and bob-cli-kj open.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.6.md) | [bob-cli-kj.6](bob-cli-kj.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@70408bf`](https://github.com/bobs-org/bob-plugins/commit/70408bf815ce899ca2e5965e9fca8c1d8703ceee) | fix(block-id-prompt): restore task-wikilink snapshot and rank CPU budgets | [bob-cli-kj.6](bob-cli-kj.6.md) | 2026-11-11 18:16:41 EST |
