# Bead: bob-cli-ft.5 — Block marks in Tasks query results (CSS-only)

[Bead Pages](../README.md) / [bob-cli-ft](README.md) / bob-cli-ft.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.16w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.16w.md) · **Assignee:** `bob-cli-ft.5` · **Size:** medium
**Created:** 2026-11-02 06:28:11 EST · **Closed:** 2026-11-02 13:06:03 EST
**Plan:** [202611/blocked\_reason\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/blocked_reason_marks.md)

## Description

tasks_results: draw the marks on Tasks query result rows from Tasks' own row attributes, with no JS on Tasks DOM. Also hide the priority glyph on digit rows and the project tag on ^ rows. Verify the Tasks 8.4.0 attributes in the e2e harness.

## Notes

[2026-11-02T18:06:03Z · bob-cli-ft.5] CSS-only Tasks query marks: BM24 medium+future paints 2; hide-priority still classifies from data-task-priority; short mode paints; toggle off restores Tasks ? then on restores 2; 0 JS data-bob-block on 59 Tasks rows; both theme screenshots; query-result scoped so source-note lis keep JS marks and BM19 pill. Real Obsidian e2e /tmp/bm-tasks-e2e6 pass=true. Manifest 1.92.0, vault synced.

## Dependencies

- **Depends on:** [bob-cli-ft.4](bob-cli-ft.4.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-ft.6](bob-cli-ft.6.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ft.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.5/README.md) | [bob-cli-ft.5](bob-cli-ft.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8c7e710`](https://github.com/bobs-org/bob-cli/commit/8c7e710306d0e49b52376e5d6d85f52dfd73f722) | docs(blocked-marks): record Tasks query CSS-only marks | [bob-cli-ft.5](bob-cli-ft.5.md) | 2026-11-02 13:07:06 EST |
| bob-plugins | [`bob-plugins@289f764`](https://github.com/bobs-org/bob-plugins/commit/289f764cba40c1f5e26f0c482d14100ff708684e) | feat(ledger-tools): paint CSS-only block marks in Tasks query results | [bob-cli-ft.5](bob-cli-ft.5.md) | 2026-11-02 13:07:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ft.5][1] | Need full notes, remaining work, and design file path | 5 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.5/README.md

<!-- sase:referenced-by:end -->
