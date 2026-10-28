# Bead: bob-cli-dd.1 — Stabilize the Highlights current-tab test

[Bead Pages](../README.md) / [bob-cli-dd](README.md) / bob-cli-dd.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-da.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.land.md) · **Assignee:** `bob-cli-dd.1` · **Size:** large
**Created:** 2026-10-27 18:53:11 EDT · **Closed:** 2026-10-27 20:17:14 EDT
**Plan:** [202610/backlog\_batch\_b3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b3.md)

## Description

mac-highlights-flake: investigate bob-cli-d4 in bob-mac-capture, repair the demonstrated synchronization race without weakening current-tab assertions, compile the Mac targets, and supply focused/full-suite macOS evidence for the lander.

## Notes

[2026-10-27T23:45:22Z · bob-cli-dd.1--1] Focused CI run 40601938746 failed on compile error RefsPanelModelTests.swift:6705 — 'operator can throw but expression is not marked with try' from 'fetcher ?? BobRefsFetcher(client: try bobClient(...))'. Fixed with explicit resolvedFetcher if/else. Re-ran macos-ci-check as snapshot f88496e0470768c1fb88dd374e430bb5a6851235, run https://github.com/bobs-org/bob-mac-capture/actions/runs/40603214971 (base 6888589). Local waiter hit 540s timeout while run still in_progress; remote branch cleaned up, run continues. Handing to monitor to watch run to completion.

[2026-10-27T23:53:23Z · bob-cli-dd.1--2] Run 40603214971 conclusion: canceled by @bbugyi200 during full Test, not a test failure. Snapshot f88496e0470768c1fb88dd374e430bb5a6851235, base 6888589, https://github.com/bobs-org/bob-mac-capture/actions/runs/40603214971 job 122536219184. Gates: Lint Swift formatting ok, Build ok, Focused Highlights current-tab repeats 20x ok, Test canceled mid-suite (RefsInspector 67 pass, RefsKeyRouter 29 pass, RefsLibrary 39 pass, RefsLinks 21 pass, then canceled in RefsListScrollHostedTests), Bundle/Verify plist+signature/Launch/Install skipped. Prior run 40601938746 failed on RefsPanelModelTests.swift:6705 missing try with ?? (fetcher ?? BobRefsFetcher(client: try bobClient)); fixed with explicit resolvedFetcher if/else. Root cause for flake: snapshot published before git backfill merged added/addedAt, so waitForModel predicates timed out; fix adds waitForGitBackfill bounded 15s wait, hasPublishedGitBackfill check on small_opened/small_book added dates, diagnosticSummary with labels on waitForModel, and new testHighlightsKeySelectsCurrentTabAfterGitBackfill holding git lane via BoundedGitGate/GatedGitFetcher. Changed: Tests/BobMacCaptureTests/RefsPanelModelTests.swift only; restored .github/workflows/ci.yml to HEAD, kept /tmp/highlights-focused-workflow.diff as temp workflow difference. Bounded-wait behavior preserved, no assertion weakening, no timeout raise as fix. Commands: gh run view 40603214971, gh run view --log --job=122536219184. Full clean-tree macos-ci-check still needed; handing to monitor.

[2026-10-28T00:17:06Z · bob-cli-dd.1--3] Full clean-tree macos-ci-check PASSED. Run https://github.com/bobs-org/bob-mac-capture/actions/runs/40605209440 (run 40605209440, job macOS 26 SwiftPM ID 122542884672, attempt 1, conclusion success, 16m39s). Base SHA 6888589d36d36b58e5d50bca48672a3e6d99e44f, snapshot SHA faab027dfe510b8da9aecc99c1142a99975bfe9f, event push on ci/precommit/16b4f8f03d4b81e5dfc06ae99b0926f1 (branch deleted after pass). Gates: Set up job ok, Check out repository ok, Check scripts ok, Show toolchain ok, Lint Swift formatting ok, Build ok, Test ok (full suite), Upload render fixtures ok, Upload test hang samples skipped, Bundle ok, Verify plist and signature ok, Launch smoke test ok, Upload launch smoke test diagnostics skipped, Install and reinstall ok. Root cause: snapshot published before git backfill merged added/addedAt (small_opened/small_book), so waitForModel predicates timed out; plus resolvedFetcher compile error (missing try with ?? at RefsPanelModelTests.swift:6705 in prior run 40601938746, fixed with explicit if/else). Fix in Tests/BobMacCaptureTests/RefsPanelModelTests.swift only (272+/8-): waitForGitBackfill bounded 15s wait, hasPublishedGitBackfill check on small_opened/small_book added dates, diagnosticSummary with labels on waitForModel, new testHighlightsKeySelectsCurrentTabAfterGitBackfill holding git lane via BoundedGitGate/GatedGitFetcher (15s timeout). Bounded-wait preserved, no weakened assertions, no timeout raise as fix. Workflow restored to HEAD (no diff); /tmp/highlights-focused-workflow.diff kept as temp workflow difference only. Commands: ./Scripts/macos-ci-check (clean tree), gh run view 40605209440 --repo bobs-org/bob-mac-capture, gh api jobs/run_attempt checks, git status/diff verification.

[2026-10-28T00:17:14Z · bob-cli-dd.1--3] Verified full clean-tree macOS CI run 40605209440 attempt 1 success (base 6888589, snapshot faab027dfe510b8da9aecc99c1142a99975bfe9f): Lint, Build, Test full suite, Bundle, Verify plist/signature, Launch smoke, Install/reinstall all passed. Only Tests/BobMacCaptureTests/RefsPanelModelTests.swift changed; workflow at HEAD.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dd.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dd.1.md) | [bob-cli-dd.1](bob-cli-dd.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@88757e9`](https://github.com/bobs-org/bob-mac-capture/commit/88757e97c4d761e4fbbf4829c1ed6badb7db36af) | test(refs): stabilize Highlights current-tab sync with bounded git backfill wait | [bob-cli-dd.1](bob-cli-dd.1.md) | 2026-10-27 20:17:50 EDT |
