# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.4 — Diagnose the RefsLibrary extra follow-up call on macOS CI

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.4` · **Size:** large
**Created:** 2026-10-26 10:47:09 EDT · **Closed:** 2026-10-26 11:19:43 EDT
**Plan:** [202610/backlog\_batch13\_vault\_integrity\_and\_perf\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch13_vault_integrity_and_perf_1.md)

## Description

refs-refresh-flake: resolve bob-cli-67 by explaining the extra ref list call on the same trigger pattern, then fixing refresh/backfill sequencing or test setup without weakening its expectation.

## Notes

[2026-10-26T15:09:10Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.4] Verified the already-landed RefsLibrary git-date lost-update fix for bob-cli-67. No product, fixture, or assertion changes in this phase.

\## Recommendation for the parent lander

Close bob-cli-67 as done, fixed by eed300d33e5296336f5b24fb56a762f283aa9048. Leave ancestors open. This phase does not close bob-cli-67.

\## Causal explanation

The original same-SHA flake on c4dc4b63062733f73678e33f65c2dc7011a4a025 (CI run 38010286522, 1 of 3 attempts) was `XCTAssertEqual failed: ("5") is not equal to ("4")` on `components(separatedBy: "argv=ref list")`. That split counts three list invocations as 4 segments; 5 means one extra git `ref list -g`.

Interleaving:

1. The first plain snapshot publishes, then starts its independent git-date pass.
2. The queued plain follow-up creates its next snapshot from the still-empty git cache and suspends in `checkFilesAndSweep`.
3. The git pass publishes its dates while that sweep is suspended.
4. Unfixed code copied git dates before the sweep await, then published the earlier empty-cache snapshot over the merge and started another git pass.

`runSnapshotPass` now copies `gitAddedDates` and `gitAddedAt` from the live snapshot after the sweep await, immediately before main-actor publication. No suspension sits between that copy and publish. If backfill finishes after publication, `runGitDatePass` merges into the latest snapshot; a queued git follow-up skips Bob when `pathsNeedingGitDates` is empty. First paint stays independent of `-g`; a git failure cannot take a good snapshot off the screen.

Historical Mac reproduction (prior investigation, `plan:202610/bob_mac_capture_latent_ci_failures.md` step 5): two git calls on unfixed code, one after the fix, 3/3 repeated runs. This turn did not re-run that harness.

\## Inspected code (this turn)

Linked checkout `sase repo open bob-mac-capture` at 7b9bbddabfd2b3368bb77287842e045f677cabb7, clean. eed300d and 7d6063a66a38e289644ef3a69a3abcad173af9a4 are ancestors. eed300d is the lost-update fix; 7d6063a later carried `gitAddedAt` through the same post-await copy.

`Sources/BobMacCapture/Refs/RefsLibrary.swift::runSnapshotPass`: both git cache fields are assigned after `checkFilesAndSweep` and before `snapshot = next`.

`Tests/BobMacCaptureTests/RefsLibraryTests.swift::testTriggersDuringRefreshRunExactlyOneFollowUp` is identical to c4dc4b6 after whitespace normalization: three immediate `.manual` refreshes, `waitUntil(timeout: 40)` for split count 4, 4s sleep, `XCTAssertEqual(..., 4)` for `argv=ref list` and 3 for `argv=plan -f json`. Expectations and timeouts were not weakened.

Regression coverage still present:

- `testSnapshotPassKeepsGitDatesMergedDuringItsSweep` (hold second sweep, release git, then sweep; dates/instants survive; `gitListCount == 1`)
- `testRefreshCarriesGitAddedAtAndSkipsASecondGitPass` (later refresh reuses date/instant cache; `gitListCount == 1`)

\## CI evidence (re-fetched this turn)

GitHub run 40334595958 attempt 1, job 121612668782 (`macOS 26 SwiftPM`), exact SHA 7b9bbdd:
https://github.com/bobs-org/bob-mac-capture/actions/runs/40334595958/job/121612668782

- Lint Swift formatting: success
- Build: success
- Test: failure (overall job)
- `testTriggersDuringRefreshRunExactlyOneFollowUp` passed (6.582s)
- `testSnapshotPassKeepsGitDatesMergedDuringItsSweep` passed (0.836s)
- `testRefreshCarriesGitAddedAtAndSkipsASecondGitPass` passed (0.748s)
- Test Suite `RefsLibraryTests`: 38 tests, 0 failures, 35.194s
- Suite total: 3119 tests, 18 failures (0 unexpected)

The 18 failures are outside RefsLibraryTests and the git-date backfill path. They do not reopen this investigation. The whole CI job is not green.

\## Validation this turn

- `just portable-check` in the linked bob-mac-capture checkout on Athena: exit 0. Pre-existing swift-format indentation warnings. `swift test` executed 1658 portable tests, 0 failures (83.297s). Does not execute macOS application XCTest.
- `just check` in bob-cli: pending at note time; follow-up records the result.
- Mac (`ssh mac`): reachable. Apple Swift 6.3.2, macOS 26.5 (25F71), `/Library/Developer/CommandLineTools`. No real XCTest (`Scripts/typecheck/XCTest.swift` is a type-check stub). No Swift source was changed, so no scratch `bundle.sh` / `just typecheck-tests` compile was required. Real XCTest evidence is the CI job above.

\## Beads

- Assigned phase bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.4 was in_progress with no prior work notes.
- bob-cli-67 remains READY for the parent lander.
- `sase bead epic-symbols bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.4`: no entries.

[2026-10-26T15:19:33Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.4--1] bob-cli just check (monitor bgyy1rmw47e1): exit 0, passed. Elapsed 5m38s. Required checks passed; no test failures. Tree unchanged for this phase. No PROPOSED FOLLOW-UP.

[2026-10-26T15:19:43Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.4--1] Verified the landed RefsLibrary lost-update fix, unchanged coalescing expectation, and exact-SHA regression results; see phase notes for SHAs, CI evidence, checks, and limitations.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.4.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md

<!-- sase:referenced-by:end -->
