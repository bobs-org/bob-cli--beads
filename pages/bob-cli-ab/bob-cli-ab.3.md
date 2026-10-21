# Bead: bob-cli-ab.3 — Calibrate thresholds and measure on the Mac

[Bead Pages](../README.md) / [bob-cli-ab](README.md) / bob-cli-ab.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.27.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.27.linker.w0.md) · **Size:** medium
**Created:** 2026-10-20 17:44:13 EDT · **Closed:** 2026-10-21 13:48:49 EDT
**Plan:** [202610/capture\_similar\_tasks\_band.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_similar_tasks_band.md)

## Previously Closed

> ↺ Closed 2026-10-21T00:50:54Z · done
>
> (none)
>
> Reopened 2026-10-21T00:52:11Z by `sase bead open`

## Description

calibrate: build the leave-one-out sampling script, collect Bryan's labels, set the bars from them, time a release build on the Mac against the 50 ms gate, and file a calibration report in the research sidecar.

## Notes

[2026-10-21T00:40:27Z · bob-cli-ab.3] PROPOSED FOLLOW-UP: Time release bob capture-related on the Mac when it is online (30 qualifying + 30 non-qualifying runs); if p95 exceeds 50 ms, file the in-app index-escalation task bead from the research and do not block

[2026-10-21T00:50:18Z · bob-cli-ab.3] PROPOSED FOLLOW-UP: Collect Bryan labels for the 100-pair calibration worksheet (0/100 filled 2026-10-21), then set bands.rs bars to possible_duplicate precision >= 80% and similar usefulness >= 60% (calibration=labels decision; do not invent researcher labels)

[2026-10-21T00:50:54Z · bob-cli-ab.3] Sampler landed: scripts/dev/capture_related_calibrate + _test wired into just check-scripts (just check-scripts green incl. new PASS; 12 capture_related unit + 1 CLI test green). Live rerun reproduces census exactly: 502 queries/0 errors, firing rates 10/24/30/42, bands 2/7/19/0/26/448, all 28 fired rows byte-identical. Bars stay at starting values per R10: worksheet labels are 0/100 (Q1 checkbox notwithstanding), so no retune; recorded as PROPOSED FOLLOW-UP. Mac still offline (SSH timeout rechecked); timing stays provisional + follow-up recorded. calibration.md updated in research sidecar (rerun table, 30-pair fix).

[2026-10-21T00:57:41Z · bob-cli-ab.3] PROPOSED FOLLOW-UP: Reconcile the completed-labels Q&A with the audited worksheet, which is still 0/100 labeled, then set thresholds from Bryan’s labels; the MacTiming “online” answer also still times out over SSH on recheck, so run the 30+30 Mac timing when reachable.

[2026-10-21T11:12:22Z · 9t] Recovery audit 2026-10-21: current master 5d212ef9 does not contain the sampler, and the calibration report/worksheet were absent from the research sidecar. Recovered sampler/test/justfile changes from bob-cli_14 stash@{0} (gh-workflow-1792544017) into this turn’s opened bob-cli checkout. Restored report from file:explicit:7c689c33d9c1d963d3dcd8f7 and worksheet from file:explicit:f1a9611f4190a723473baade; it still has 0/100 labels. Earlier completed-label answers were auto-selected question choices, not submitted labels. Mac SSH now works (arm64, macOS 26.5); preparing the release timing run. Replaced GNU date timing with Python monotonic subprocess timing and fixed nested output-directory rejection to avoid creating a directory inside the vault. just check-scripts passes.

[2026-10-21T11:34:25Z · 9t--1] Mac verification monitor jkc6bnty6yd9 passed (release timing + just check + just check-scripts). Mac arm64/macOS 26.5: qualifying n=30 median 40.700 ms, p95 46.881 ms; non-creating n=30 median 6.461 ms, p95 7.547 ms. Warmed 50 ms gate passes; first qualifying warmup was 968 ms, recorded separately. Installed binary checksum and clean vault status unchanged; scratch removed. Evidence file:explicit:416e5e7515b42bf9c399706f. Corrected report false claims: old worksheet has only 54 matching rows / 30 unordered pairs and 46 blank candidates, still zero labels. Fixing sampler self-suppression of closed rows with query-only --exclude NOTE:LINE plus real-pair stratification; full verification/rerun follows. Thresholds remain provisional and this bead stays open pending actual Bryan labels.

[2026-10-21T11:46:53Z · 9t--2] Verification recovery: qf78rnrrmt3k failed only at the new draft-mode exclusion assertion. Added an explicit exclude/draft conflict; the full calibration exclusion regression now passes (ToolRun 01bc62ea5c7ff50c7145ebbadeb10265). Added completion value metadata for --exclude and updated calibration.md with the result. A monitored release rebuild, corrected live census/worksheet, docs generation, just check, check-scripts, and docs-check follows. Actual labels are still zero; thresholds remain provisional and the bead remains open.

[2026-10-21T12:08:52Z · 9t--3] Verification monitor 69d605qf0vva completed exit 0: release build, corrected live census, docs-gen, just check, check-scripts, docs-check, and diff-check all passed (ToolRun 4f943c0d1f94c70c8e79574de8be6d79). Audited census: 496 queries / 53 routes / zero errors; visible starting-band firing 33/496 (6.7%). Worksheet contains every returned candidate: 80 real directed pairs / 48 unordered pairs, including 6 closed candidates, with 0/80 labels. No blanks or self-matches; review IDs and source hashes verified. Apollo qualifying median/p95 86.406/90.935 ms; prior Mac warmed p95 remains 46.881 ms. Updated report file:explicit:4b45a63b6333b9258375bd48. Human review file:explicit:bd9fe71a265c714e4f41578a; CSV file:explicit:965954f61a5d725b7827ed11; census file:explicit:c9ad49e5fc63d54df5ba9edd; full responses file:explicit:12ffdbf73c4f258517bdb94e. Next: free-text sase_questions handoff requesting actual numbered D/U/N judgments or labeled-file location. No options that can auto-claim completed labels. Calibration=labels remains required; no retune or close until actual evidence supports acceptance. Source and research changes remain in the opened external checkouts for host finalization after the label continuation.

[2026-10-21T16:29:46Z · 9t--4] Bryan explicitly delegated pair labeling in gate bb385582-380e-4885-b381-3cb6422909db (answered 2026-10-21T16:19:32Z) and requested opus@xhigh to double-check then complete the work. This supersedes the earlier requirement to obtain human-authored labels; these remain agent judgments, not Bryan labels. First pass: all 80 pairs labeled before inspecting per-pair scores, with rationale/confidence; 10 D / 46 U / 24 N across 48 unordered relationships (6 D / 27 U / 15 N). Current possible_duplicate precision 6/10=60%; Similar usefulness 15/21=71.4% (rank-one 10/15); closed duplicate precision 2/6. Same-title docs pairs concern different products. Visible firing remains 33/496=6.7%. Thresholds unchanged and bead remains open for Opus review/calibration. All identities, titles, scores, bands and ranks checked against retained responses; reverse labels agree. Source code unchanged this turn; prior gates stand, both diff checks pass. Evidence: labels/rationale file:explicit:b27592e2a9e2fdfe6a2165a2; CSV file:explicit:ef1d9faf9c1efce6c084ba23; provenance file:explicit:3909e4a260d0f8aea117a8bc; preliminary analysis file:explicit:78fd69bc548396bd7b4bd609; metrics JSON file:explicit:ff62ac5ae34daa9125d5ba5b; updated report file:explicit:0425e6ab9241cb0c0562038f. Handing off as explicitly requested; source/research changes still require host finalization by the completing turn.

[2026-10-21T17:48:25Z · 9t--4] PROPOSED FOLLOW-UP: For the decisions record (bob-cli-ab.8) — same_title is a literal-equality contract. The only observed same-title rows (one relationship, pairs 14/26) are the same docs-site wish in Bob and SASE, judged useful heads-up, not duplicates. So the plan-selected discard default for same_title is a product decision this data neither supports nor refutes. Separately, closed_duplicate stays at the duplicate bar 0.70 with 2 D / 2 U / 0 N; re-check it once more closed pairs accumulate (a bar above 0.82 would read 2/2, but rests on one pair). Evidence: file:explicit:0c5ba774dc98d448c2a9d408

[2026-10-21T17:48:33Z · 9t--4] PROPOSED FOLLOW-UP: Abbreviation-aware matching (appt vs appointment) only if future labels show recurring misses. The CT appointment duplicates (pairs 6/48) now surface as similar, not possible_duplicate. No vocabulary table was added during calibration. Evidence: file:explicit:c36bed37d6fb0b0a1ed456ef

[2026-10-21T17:48:49Z · 9t--4] Calibrated from reviewed agent labels under Bryan's delegation (gate bb385582-380e-4885-b381-3cb6422909db); these are not Bryan-authored labels.

Label review: I labeled all 80 pairs blind before reading the first pass and agreed on 79/80. Pair 51 was revised N->U (low confidence). Reviewed totals are 10 D / 47 U / 23 N (6/28/14 unordered). Nine newly exposed pairs were labeled 7 U / 2 N; every visible row at the final bars is labeled.

Changes:
- Tokenizer: closed-class function-word stopwords; single-digit numbers kept as terms.
- Number guard: titles whose number sets differ cannot be possible_duplicate or closed_duplicate.
- SIMILAR 0.55->0.48. POSSIBLE_DUPLICATE, CLOSED_DUPLICATE, hold margin and short-query rules are unchanged.

Results on the 496-query census, rerun through real builds on a read-only snapshot of the labeled vault state (6af37e5e, reproduced exactly):
- possible_duplicate precision 6/10 -> 6/6 (Wilson 61-100%; 3 relationships).
- similar usefulness 39/54 = 72.2% (first-pass labels 70.4%; low-confidence flipped 63.0%; capture-like subset 65.0%).
- Firing 6.7% -> 11.1% (capture-like 10.0%).
- Closed duplicates 2 D / 2 U / 0 N.
- Live-vault cross-check: 55/489 = 11.2%, same label counts.
These are in-sample, not held-out.

Mac (Kellys-MBP arm64), calibrated release build: qualifying median 41.436 ms, p95 43.494 ms (<= 50 ms gate). Installed bob and vault status unchanged; scratch removed.

Gates passed on the final tree: docs-gen (no new changes); just check (5268 tests, 0 failed); check-scripts; docs-check (447 passed, 1 skipped; rerun after a doc line re-wrap); git diff --check.

Report: file:explicit:0c5ba774dc98d448c2a9d408. Labels: file:explicit:c7de83cce58aab48e84b27a1 and file:explicit:773fbd5a6f26c5e990c6244a. Analysis: file:explicit:c36bed37d6fb0b0a1ed456ef. Mac timing: file:explicit:b665608a7bbb39d1288d4bba.

Source and research changes are uncommitted in the opened bob-cli and bob-cli--research checkouts; they are committed through host finalization.

## Dependencies

- **Depends on:** [bob-cli-ab.2](bob-cli-ab.2.md) ✓ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-ab.8](bob-cli-ab.8.md) ✓ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ab.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ab.3.md) | [bob-cli-ab.3](bob-cli-ab.3.md) | 0 |
