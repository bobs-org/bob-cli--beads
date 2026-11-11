# Bead: bob-cli-kj.6 — Task-wikilink CPU budget investigation

[Bead Pages](../README.md) / [bob-cli-kj](README.md) / bob-cli-kj.6

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bm](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bm.md) · **Assignee:** `bob-cli-kj.6` · **Size:** large
**Created:** 2026-11-11 17:20:04 EST
**Plan:** [202611/impact\_ranked\_bead\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/impact_ranked_bead_fixes.md)

## Description

wikilink-perf: establish reproducible measurements for the block-id-prompt task-wikilink snapshot/order and keystroke-rank CPU budget failures, then land a production fix, measurement fix, or justified budget — never a silent bump (bead bob-cli-f8).

## Notes

[2026-11-11T22:41:17Z · bob-cli-kj.6] PLANNING EVIDENCE: No earlier phase notes or landed repair found; bob-plugins e8a776ee909e38aaeb2031e26197b6dc0522189e retains the f0c1c97 ranker/test and original index decoration. Unmodified focused test on athena Node v20.19.2: 3/5 pass, snapshot/order 74.4 ms > 50 and rank 13.9 ms > 12. Identical source bytes evaluated through SSH stdin on apollo Node v18.19.1: 3/5 pass, 95.2 ms and 16.8 ms respectively; no remote repo reads or writes. Both use process.cpuUsage fallback, not thread CPU. In-memory ablations implicate spread-plus-appended snapshot row properties and cached search-field order: fresh Object.assign copy plus search-text-first fields yielded snapshot/order 18.56–30.76 ms and rank 1.32–11.22 ms over seven sequential samples. A fresh athena process using only that decorateRow substitution passed the original 5/5 performance tests. Source/test files remain unchanged. A medium tale is validated for the local production repair, real cached-versus-uncached parity tests, profiling, repeated cross-host controls, full gates and sync; implementation is deferred only to the explicitly requested plan approval, not an oversized unfinished coding attempt. No epic-symbol entries currently exist. Preliminary measurements are not final acceptance evidence.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kj.6.md) | [bob-cli-kj.6](bob-cli-kj.6.md) | 0 |
