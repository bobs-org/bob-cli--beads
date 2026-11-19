# Bead: bob-cli-nj.5 — bob-mac-capture: pull-in cancel reason recall

[Bead Pages](../README.md) / [bob-cli-nj](README.md) / bob-cli-nj.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.f3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.f3.md) · **Assignee:** `bob-cli-nj.5` · **Size:** medium
**Created:** 2026-11-19 12:14:03 EST · **Closed:** 2026-11-19 14:52:32 EST
**Plan:** [202611/log\_reason\_recall.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/log_reason_recall.md)

## Description

mac-cancel-recall: in CaptureCore, decode the `bob logs list` JSON and add the ranking (tested against the vendored vectors), the recall state, and the band presentation. Add a gated 3-row USED BEFORE band under CapturePullInReasonField, plus router Ctrl+N/P and ↑/↓, Esc layering, and the blur guard. Gate on exact-SHA macOS CI.

## Notes

[2026-11-19T19:52:20Z · bob-cli-nj.5] PROPOSED FOLLOW-UP: just docs-check fails at source-context assembly (bob-plugins mount index.md collides with committed reference/plugins/index.md), reproduces identically on the clean base tree via stash, so it is environmental and unrelated to this phase; land agent to confirm the docs gate on the push CI run

[2026-11-19T19:52:32Z · bob-cli-nj.5] Implemented mac-cancel-recall: CaptureCore LogRecallCatalog/Ranking/State/BandPresentation (vectors vendored byte-identical, every vector run in tests), BobProcessClient logHistory on log-history lane with per-executable unsupported memory, router Ctrl+N/P + Up/Down to recallNext/PreviousPullInReason, model recall session with Esc layering + blur guard + stale-while-revalidate fetch on reason open, USED BEFORE band under CapturePullInReasonField with card+panel height, docs updated with Log Recall link. Verified: swift format lint exit 0, swift build exit 0, swift test 2621 pass 0 fail (27 new LogRecall tests) on athena; docs-check fails identically on clean base (environmental, noted as follow-up). Not verified: BobMacCapture macOS targets (mac offline) and exact-SHA macOS CI (no commit/push from phase worker; left for land agent).

## Dependencies

- **Depends on:** [bob-cli-nj.1](bob-cli-nj.1.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nj.7](bob-cli-nj.7.md) ◐ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.5/README.md) | [bob-cli-nj.5](bob-cli-nj.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e58a9e2`](https://github.com/bobs-org/bob-mac-capture/commit/e58a9e27e6649b8498fb411a4a3aca87a2a3c60a) | feat(capture): pull-in cancel reason recall from vault log history | [bob-cli-nj.5](bob-cli-nj.5.md) | 2026-11-19 14:54:12 EST |
