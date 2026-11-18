# Bead: bob-cli-ms.8.3.1.1 — Prove record sheet rendering and fix Properties hiding in real Obsidian

[Bead Pages](../README.md) / [bob-cli-ms.8.3.1](bob-cli-ms.8.3.1.md) / bob-cli-ms.8.3.1.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ms.8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.8.3.md) · **Assignee:** `bob-cli-ms.8.3.1.1` · **Size:** medium
**Created:** 2026-11-18 08:59:24 EST
**Plan:** [202611/record\_card\_obsidian\_proof.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card_obsidian_proof.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:09ac8f1ecf45e0f8ddb8b199 | attached via sase artifact create --bead |
| related | file:explicit:2d289bd2417cd27d4dd5c48c | attached via sase artifact create --bead |
| related | file:explicit:36bbab23c7b6af310f23ac9e | attached via sase artifact create --bead |
| related | file:explicit:769e949c1dbb69085e10b4c5 | attached via sase artifact create --bead |
| related | file:explicit:a95227eb6d04ff49fc29fa6a | attached via sase artifact create --bead |
| related | file:explicit:bed2e0d97ccd3a2624288065 | attached via sase artifact create --bead |
| related | file:explicit:c57752fb786326f0222d5286 | attached via sase artifact create --bead |
| related | file:explicit:e28e8d1413ec5b4b13bfb89e | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

sheet-dom: build the isolated Record Card CDP runner and offline wrapper, prove the sheet and native Properties lifecycle on athena, and fix defects using captured DOM evidence and regression tests.

## Notes

[2026-11-18T19:12:18Z · bob-cli-ms.8.3.1.1--a] Phase-one evidence and gate status — 2026-11-18

Real Athena Obsidian acceptance run 21 passed: 89 mandatory assertions passed, 0 failed, with the 2 phase-two assertions skipped as out of this phase scope. Run report artifact: file:explicit:bed2e0d97ccd3a2624288065. The six visually inspected screenshot artifacts are: frontmatter-only reading file:explicit:769e949c1dbb69085e10b4c5; live dark wide file:explicit:2d289bd2417cd27d4dd5c48c; folded properties open file:explicit:09ac8f1ecf45e0f8ddb8b199; live light 375px file:explicit:a95227eb6d04ff49fc29fa6a; collapsed file:explicit:c57752fb786326f0222d5286; live light wide file:explicit:e28e8d1413ec5b4b13bfb89e. Deployed-vault startup smoke report artifact: file:explicit:36bbab23c7b6af310f23ac9e.

Record Card focused tests passed 94/94. Plugin build and build:check passed. Validate passed with all 11 manifests valid; docs inventory passed; docs:check passed, including 447 documentation tests and 1 expected dependency/font skip. Obsidian startup smoke unit tests passed 17/17; smoke help passed. Real pre-sync smoke passed. Post-sync deployed-vault smoke passed against /home/bryan/bob: layout-ready 365 ms, heap peak 46.8 MiB, all 4 editor cases passed, 0 exceptions, 0 rejections, and 0 crash artifacts. The no-force sync followed the deployment runbook after the protection refusal: fetched, fast-forwarded the landed commit 21cf4f9, cleaned and rebuilt, restored the phase changes, previewed, then synced without force. Post-sync dry run reported all 11 plugins up to date. bob plugins list still reports the known bob-emoji vault Git tracking warning.

The full plugin npm test gate is not green. It exited 1 with 7,309 passing, 4 failing, and 3 skipped unit tests; the 5-test perf suite passed. The four failures were 25 ms performance budgets in event-link-times, frees-marks, keep-moving-marks-surface, and off-clock-link-chips. The same four files passed when rerun serially: 110/110. This does not change the failed full npm test result.

sase bead epic-symbols bob-cli-ms.8.3.1.1 passed with no entries. The requested bob-cli just check has not yet completed and will be staged through sase monitor. Because the full plugin npm test gate failed and just check is pending, this phase remains in_progress and is not being closed. bob-cli-ms.8.3.1.2 remains in_progress and unchanged.

[2026-11-18T19:47:20Z · bob-cli-ms.8.3.1.1--c] 2026-11-18 gate update: the repaired bob-cli `just check` passed; all 7,361 Rust tests and the rest of the recipe completed successfully. The required full bob-plugins `npm test` rerun remains red (monitor h1rzdhqtpazc, ToolRun 011dbb7aa779f859f49fc0963defa96a; diagnostic-manifest and retained-log refs attached above). `test:unit` reported 7,309 pass, 4 fail, 3 skipped; its separate `test:perf` suite passed 5/5. Exact failed wall-clock assertions: event-link-times 104.1 ms against 25 ms; frees-marks 174 ms against 25 ms; keep-moving-marks-surface 2,803.2 ms against its 250 ms assertion; off-clock-link-chips 164.5 ms against 35 ms. The `test:unit` script invokes `node --test` without an explicit file-concurrency limit. The prior serial rerun of these four files passed 110/110, so runner contention is plausible, though the measurements do not prove the cause. No code change was made. Because the required full plugin gate failed, this phase remains in_progress; bob-cli-ms.8.3.1.2 remains in_progress.

## References

- file:monitor-diagnostic-manifest:h1rzdhqtpazc
- file:monitor-retained-log:h1rzdhqtpazc

## Dependencies

- **Blocks:** [bob-cli-ms.8.3.1.2](bob-cli-ms.8.3.1.2.md) ◐ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.8.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.1.md) | [bob-cli-ms.8.3.1.1](bob-cli-ms.8.3.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8e8ff51`](https://github.com/bobs-org/bob-plugins/commit/8e8ff51f97732c5ad737215ee5bb2a78350db5ef) | feat(record-card): add record sheet and interaction coverage | [bob-cli-ms.8.3.1.1](bob-cli-ms.8.3.1.1.md) | 2026-11-18 15:09:18 EST |
