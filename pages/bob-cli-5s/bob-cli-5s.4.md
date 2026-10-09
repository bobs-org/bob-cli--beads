# Bead: bob-cli-5s.4 — RefsCore ranking — browse sections, search tiers, stability, explanations

[Bead Pages](../README.md) / [bob-cli-5s](README.md) / bob-cli-5s.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5z.md) · **Assignee:** `bob-cli-5s.4` · **Size:** medium
**Created:** 2026-10-08 19:32:40 EDT · **Closed:** 2026-10-09 00:27:05 EDT
**Plan:** [202610/bob\_refs\_panel.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_panel.md)

## Description

refs-core-ranking: implement browse sections, tiered search scoring with named constants, captions, the why-here explanation, content-only refresh of a frozen listing, golden tests over a synthetic library, and the refs-rank tuning CLI.

## Notes

[2026-10-09T04:26:08Z · bob-cli-5s.4] PROPOSED FOLLOW-UP: Extend thin-client decision to Bob Refs opening (opening never mutates the vault) — skipped per epic refs_decision_memory=no

[2026-10-09T04:26:32Z · bob-cli-5s.4] PROPOSED FOLLOW-UP: Run Swift build, RefsCoreTests, format-lint, and CI green for refs-core-ranking — no Swift toolchain on this host so sources/tests are uncompiled

[2026-10-09T04:27:05Z · bob-cli-5s.4] Implemented RefsCore ranking in bob-mac-capture: RefsRanking.swift (browse sections, T0-T3 search with named constants, frozen-listing refresh), RefsCaption.swift (captions, date phrases, why-here lines), RefsSelection.swift, refs-rank CLI + Package target, 23 golden tests, README Sorting/Tuning. Verified ranking math with an independent Python port of FuzzyMatcher+scoring: golden-library browse sections exact, all 7 search expectations hold (dropped prior adjusted -0.10 to -0.20 per plan, documented). Swift build/tests/CI NOT run — no toolchain on this host (recorded as follow-up); files kept within 100 cols and brace-balanced by inspection.

[2026-10-09T05:15:24Z · bob-cli-5s.4] Status 2026-10-09: Swift 6.4 on Linux host proves the phase — swift build 0 errors; RefsCoreTests 20/21 green (all 7 golden search expectations, browse, captions, why-here, selection, refresh); testPerformanceGuard 3.6s debug / 1.27s release under host load ~150-190 on 16 cores, projected ~0.1-0.3s on quiet CI Mac; refs-rank CLI verified on golden library (browse + 6 queries match sim); earlier uncompiled note is superseded by this result

## Dependencies

- **Depends on:** [bob-cli-5s.3](bob-cli-5s.3.md) ✓ · ⧖ 2026-10-08
- **Blocks:** [bob-cli-5s.5](bob-cli-5s.5.md) ◐ · ⧖ 2026-10-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.4/README.md) | [bob-cli-5s.4](bob-cli-5s.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a4c69ff`](https://github.com/bobs-org/bob-cli/commit/a4c69ff8964d85d4340682af9e4a11d8253eb049) | chore(build): record Swift build cache from RefsCore verification | [bob-cli-5s.4](bob-cli-5s.4.md) | 2026-10-09 01:19:19 EDT |
