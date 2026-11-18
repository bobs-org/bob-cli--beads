# Bead: bob-cli-ms.8.3.1.1 — Prove record sheet rendering and fix Properties hiding in real Obsidian

[Bead Pages](../README.md) / [bob-cli-ms.8.3.1](bob-cli-ms.8.3.1.md) / bob-cli-ms.8.3.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ms.8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.8.3.md) · **Assignee:** `bob-cli-ms.8.3.1.1` · **Size:** medium
**Created:** 2026-11-18 08:59:24 EST · **Closed:** 2026-11-18 18:01:25 EST
**Plan:** [202611/record\_card\_obsidian\_proof.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card_obsidian_proof.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:09ac8f1ecf45e0f8ddb8b199 | attached via sase artifact create --bead |
| related | file:explicit:2d289bd2417cd27d4dd5c48c | attached via sase artifact create --bead |
| related | file:explicit:32c4800323de3318e872cd4a | attached via sase artifact create --bead |
| related | file:explicit:36bbab23c7b6af310f23ac9e | attached via sase artifact create --bead |
| related | file:explicit:69e78b5146f8344dfbee4b8d | attached via sase artifact create --bead |
| related | file:explicit:769e949c1dbb69085e10b4c5 | attached via sase artifact create --bead |
| related | file:explicit:a95227eb6d04ff49fc29fa6a | attached via sase artifact create --bead |
| related | file:explicit:b06414849f893e4e157517c7 | attached via sase artifact create --bead |
| related | file:explicit:b95c3d1b4c03960a27a905fd | attached via sase artifact create --bead |
| related | file:explicit:bed2e0d97ccd3a2624288065 | attached via sase artifact create --bead |
| related | file:explicit:c42d353930bd8de15dfec953 | attached via sase artifact create --bead |
| related | file:explicit:c57752fb786326f0222d5286 | attached via sase artifact create --bead |
| related | file:explicit:db1f2dd2bb9e80837e28c708 | attached via sase artifact create --bead |
| related | file:explicit:de81e51339d94e94b2928979 | attached via sase artifact create --bead |
| related | file:explicit:df22f4eb9a1dc88cb430e953 | attached via sase artifact create --bead |
| related | file:explicit:e28e8d1413ec5b4b13bfb89e | attached via sase artifact create --bead |
| related | file:explicit:e6af3da4c2cf3cca7a5e83be | attached via sase artifact create --bead |
| related | file:explicit:ecedee8cd441a00ce81a2254 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

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

[2026-11-18T20:50:57Z · bob-cli-ms.8.3.1.1] 2026-11-18 screencast repair: earlier sheet/CDP work is landed in bob-plugins 8e8ff51; integrated subsequent record-walk commit 281ee8a rather than rebuilding it. New explicit user requirement overrides the earlier whole-Properties hide: only title plus album-schema rows represented by the record card hide; parent/type/created, legacy/unknown keys and Add property remain native. Added bounded native-row ownership and a DOM replacement/key-change observer with cleanup on gate loss, view destruction and disable. Added regression tests and per-key CDP checks, including file/mode/type/parent return and a real tab-header click. Bumped ledger-tools to 1.136.0, regenerated bundle/inventory; bundle byte comparison after upstream integration matches fragments exactly. node --test scripts/test-ledger-tools-record-sheet.cjs scripts/test-obsidian-record-card-e2e.cjs scripts/test-ledger-tools-record-walk.cjs passes 40/40. No memory files changed. No epic-symbol entries. Remaining work is bounded verification/deployment, not another implementation epic: .build/property-hiding/verify.py runs full plugin gates, clean-base comparison on npm failure, current bob just check/build, isolated Athena proof/startup smoke, and non-force sync plus deployed-vault smoke only after required evidence passes. Outputs go to .build/property-hiding/verification/summary.json and results/. A monitor successor must inspect every screenshot, register audited artifacts, fix any introduced failures, and close only this bead. Known parent-listed timing failures must not strand this phase again; compare baseline evidence and honor the user closure instruction. Phase two and ancestor beads remain unchanged.

[2026-11-18T22:08:41Z · bob-cli-ms.8.3.1.1--1] Recovery of monitor fr2mj57spd75: the earlier real Obsidian run tested the old 1.135.1 bundle, because git bundle omitted the uncommitted repair. Its 88 passing assertions and one failed delimiter assertion are old-build diagnostics, not acceptance of selective Properties hiding. All six screenshots were visually inspected: card layouts are readable, but the native Properties panel and Add property are absent and fail the new requirement. Exact reports, all screenshots, and per-image verdicts are preserved below.

Integrated upstream record-walk rail e7d82af and moved selective-row ownership into its Live Preview builder. Only title and album-schema keys represented by the card hide; parent/type/created/legacy/unknown keys and Add property remain native. Added actual Add property probes, a delimiter-position check that tolerates the managed walk footer, and a regression for a failed sheet build: native rows remain visible, the failure is not cached, and a later successful build recovers. Ledger-tools remains 1.136.0. Rebuilt generated main.js; all 51 focused sheet/walk/harness tests pass, as does git diff --check. No CLI or memory files changed.

PROPOSED FOLLOW-UP: Existing bob-cli-lp flake corroborated by the earlier full npm test — MN click cursor/focus assertion failed with an empty cursor list; isolated relation-chip suites pass 27/27 on both the repaired tree and clean 281ee8a. Land agent should attach this evidence to the existing tracker, not create duplicate work. The two other full-suite timing failures already reproduced on the clean base and are covered by the parent's known-red policy.

PROPOSED FOLLOW-UP: Confirm integration of the already-recorded bob-cli-nb.1 lint correction — unchanged clean bob-cli 6cb387bc failed just check at albums/report.rs:497, unnecessary_lazy_evaluations on then(||...). Closed bob-cli-nb.1 note 3 records the mechanical then_some correction and passing subsequent gates. This clean-base failure does not hold the Properties phase open.

The docs gate timed out building Bob. Its later successful binary was recovered from the owned Athena snapshot after the prior temporary local target was removed; SHA256 a8fc562ff3a4c0a61878d821316a1485dc5844a71bb2440f9c73c9561ca788f0 is unchanged. The prepared finish.py uses that exact BOB_BIN for docs, hashes every transferred plugin source file, and records dirty-source provenance if needed. A clean e7d82af deployment preview reports 0 to copy, 3 unchanged: the protected deployed rail build has landed, and the scripted recovery uses only the documented no-force restamp.

Remaining work is the corrected real proof and required deployment gates in .build/property-hiding/finish.py, writing .build/property-hiding/final-verification/summary.json. Review every new screenshot, publish new acceptance reports, then close only this phase. epic-symbols reports no entries. Phase two and ancestors remain unchanged. The earlier diagnostics are:

summary.json: file:explicit:32c4800323de3318e872cd4a
record-proof.json: file:explicit:69e78b5146f8344dfbee4b8d
presync-smoke.json: file:explicit:ecedee8cd441a00ce81a2254
visual-review.json: file:explicit:c42d353930bd8de15dfec953
record-sheet-frontmatter-only-reading.png: file:explicit:e6af3da4c2cf3cca7a5e83be
record-sheet-fold-open.png: file:explicit:b95c3d1b4c03960a27a905fd
record-sheet-live-dark-wide.png: file:explicit:db1f2dd2bb9e80837e28c708
record-sheet-live-light-375.png: file:explicit:b06414849f893e4e157517c7
record-sheet-live-light-wide.png: file:explicit:df22f4eb9a1dc88cb430e953
record-sheet-collapsed.png: file:explicit:de81e51339d94e94b2928979

[2026-11-18T22:23:32Z · bob-cli-ms.8.3.1.1--2] Recovery of monitor xzvg05kqagm0: exact-source ledger-tools 1.136.0 passed 49 assertions before two harness failures. The Live Preview delimiter target was inside Obsidian's native Properties replacement; an isolated real Obsidian probe confirmed target 158 clamps to 159 in Live Preview and reaches 158 in Source. The runner now checks the body boundary in Live Preview and the delimiter in Source, recording actual cursor offsets. The hover selector had picked the new record-walk-arm instead of the authored body link; the corrected authored list-link selector opens the real native Properties popover. No product failure is waived.

All six final-verification screenshots were individually inspected. Native type/parent/created/legacy/unknown rows and Add property remain visible, while title/schema duplicates hide. Light/dark, 375px, collapsed/expanded card and legacy fold are readable; the new walk rail is preserved. This is diagnostic evidence only because later lifecycle checks and deployment did not run. Visual verdict: file:explicit:b866ed001ef9b78d89fe18aa. The raw re

… and 14560 more characters

## References

- file:monitor-diagnostic-manifest:h1rzdhqtpazc
- file:monitor-retained-log:h1rzdhqtpazc

## Dependencies

- **Blocks:** [bob-cli-ms.8.3.1.2](bob-cli-ms.8.3.1.2.md) ◐ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.8.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.1.md) | [bob-cli-ms.8.3.1.1](bob-cli-ms.8.3.1.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8e8ff51`](https://github.com/bobs-org/bob-plugins/commit/8e8ff51f97732c5ad737215ee5bb2a78350db5ef) | feat(record-card): add record sheet and interaction coverage | [bob-cli-ms.8.3.1.1](bob-cli-ms.8.3.1.1.md) | 2026-11-18 15:09:18 EST |
| bob-plugins | [`bob-plugins@395088a`](https://github.com/bobs-org/bob-plugins/commit/395088ab817187f9d1a3651634166d515f4cad49) | fix(ledger-tools): preserve selective record properties hiding | [bob-cli-ms.8.3.1.1](bob-cli-ms.8.3.1.1.md) | 2026-11-18 18:02:26 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ms.8.3.1.1--c][1] | Verify the phase remains open and the gate evidence was appended without replacing earlier references | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.1.md

<!-- sase:referenced-by:end -->
