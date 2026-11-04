# Bead: bob-cli-go.11 — Capture-complete and capture-rewrite for transfer lines

[Bead Pages](../README.md) / [bob-cli-go](README.md) / bob-cli-go.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.36.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.36.linker.w0.md) · **Assignee:** `bob-cli-go.11` · **Size:** medium
**Created:** 2026-11-03 16:11:31 EST · **Closed:** 2026-11-04 10:26:17 EST
**Plan:** [202611/task\_move\_merge\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_move_merge_split.md)

## Description

transfer-assist: complete sources, destinations, `+` merge targets, and `#` drawers or sections on transfer lines, extend separator rewrite and the `@@` notice, and document both.

## Notes

[2026-11-04T15:25:59Z · bob-cli-go.11] PROPOSED FOLLOW-UP: three timing-sensitive gates flaked once each under full parallel-suite load and passed immediately alone on this tree — capture::related::draft_related_stays_under_the_debug_perf_gate, stats::completion_includes_worked, stats_clock::completion_lists_only_canonical_clock_values_with_descriptions. None touch transfer paths; consider raising their load margins.

[2026-11-04T15:26:17Z · bob-cli-go.11] transfer-assist done: completion routes transfer lines through Route/Task/Drawer/Section with source narrowing to movable-or-mergeable rows, minus-source merge targets carrying a ⤵ merge consequence, the + hint warning on complete bare destinations, and section creation plus §3.4 near-duplicate refusal; rewrite switches :/^ to + in transfer slots and refuses bare @ on transfers with the capture-transfer notice; docs/capture.md, json-outputs, help text, and regenerated CLI reference updated. Verified: 8 new lib tests, 6 new CLI tests, full lib suite (4950) green, full CLI suite green except load flakes that pass alone (noted as follow-up), clippy gate clean, fmt clean.

## Dependencies

- **Depends on:** [bob-cli-go.10](bob-cli-go.10.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.12](bob-cli-go.12.md) ◐ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.11/README.md) | [bob-cli-go.11](bob-cli-go.11.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`96a3c74`](https://github.com/bobs-org/bob-cli/commit/96a3c744e63e1aef287fee630bb40c95d68e9c8f) | feat(capture): add transfer-assist completion, engine scoping, and rewrite | [bob-cli-go.11](bob-cli-go.11.md) | 2026-11-04 10:41:08 EST |
