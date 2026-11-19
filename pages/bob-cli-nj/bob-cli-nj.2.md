# Bead: bob-cli-nj.2 — bob-plugins: recall store, model, band decorator, and the Work Log modals

[Bead Pages](../README.md) / [bob-cli-nj](README.md) / bob-cli-nj.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.f3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.f3.md) · **Assignee:** `bob-cli-nj.2` · **Size:** medium
**Created:** 2026-11-19 12:14:03 EST · **Closed:** 2026-11-19 15:30:43 EST
**Plan:** [202611/log\_reason\_recall.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/log_reason_recall.md)

## Description

recall-core: add a ledger-tools `api.logs` store (stale-while-revalidate plus a session overlay) and nav's pure model and `attachLogRecall` band decorator with styles. Expose `api.logRecall` v1 and wire TaskLinkLanePromptModal, LaneReleaseSummaryModal (which also gets the standard preview and footer), and block-id-prompt's WorkSummaryPromptModal.

## Notes

[2026-11-19T20:29:31Z · bob-cli-nj.2] PROPOSED FOLLOW-UP: Trim Mac Capture capture-previews and keyboard references below the 6000-word cap — latest docs:check on bob-cli master ddf28f6 still reports 6096 and 6027 words; existing tracker bob-cli-jz was corroborated after its close.

[2026-11-19T20:30:08Z · bob-cli-nj.2] PROPOSED FOLLOW-UP: Stabilize full-suite timing gates in bob-cli-km and bob-cli-io — this npm test run measured event-link-times at 148.5 ms and frees-marks at 111 ms against 25 ms, while isolated clean-base runs passed at 20.3/23.6 ms; independent reports were added to both existing trackers.

[2026-11-19T20:30:43Z · bob-cli-nj.2] Implemented and deployed api.logs, the log-recall model/band and v1 API, Work Log modal integration, and successful-write noteUsed hooks. Build/build:check, docs inventory, and the final 154 focused tests pass. Full npm test was run before merging the upstream Copy Card C-row landing and reported the stale row-order assertion plus known km/io load timing failures; the final focused run includes and passes the corrected Copy Card model tests. Latest docs:check still fails only on Mac Capture reference budgets (6096/6027), recorded on bob-cli-jz and as a proposed follow-up here. epic-symbols reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-nj.1](bob-cli-nj.1.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nj.3](bob-cli-nj.3.md) ◐ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-nj.4](bob-cli-nj.4.md) ◐ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nj.2/README.md) | [bob-cli-nj.2](bob-cli-nj.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@795fad3`](https://github.com/bobs-org/bob-plugins/commit/795fad3d924de86eb3e3f5890ba4d467833d80bb) | feat(log-recall): add Work Log phrase recall to Obsidian prompts | [bob-cli-nj.2](bob-cli-nj.2.md) | 2026-11-19 15:33:44 EST |
